### Title
Improve FITS compressed image performance and Dask integration in `io.fits`.

### Project Team
Stuart Mumford
Thomas Robitaille
Drew Leonard

### Project Description

This project aims to increase performance of `io.fits` especially around large
compressed image data.

#### Compressed Image Performance

Currently when using tiled FITS compression the Astropy implementation loads
all the tiles into RAM and decompresses them all.
This is highly CPU and memory inefficient, and is one of the reasons Astropy is
significantly slower at loading these types of files than the `cfitsio` package
(which uses the same C library as Astropy for this currently).

For example we can compare the loading times of `io.fits` vs [`fitsio`](https://github.com/esheldon/fitsio):

<details>
<summary>Setup Code</summary>

```python
import os
from pathlib import Path

import fitsio
from astropy.io import fits
import astropy.units as u

filename = "VISP_2022_06_17T19_17_52_516_00630205_U_BLQRA_L1.fits"
path = Path("~/dkist_data/BLQRA").expanduser() / filename

fio = fitsio.FITS(path)
```

</details>

```python
# Filesize
print((os.stat(path).st_size * u.byte).to(u.Mibyte))
```
```
2.04071044921875 Mibyte
```

```python
raw_hdul = fits.open(path, disable_image_compression=True)
header = raw_hdul[1].header

print(f"{header['ZNAXIS1']=}")
print(f"{header['ZNAXIS2']=}")
print(f"{header['ZNAXIS3']=}")
print(f"{header['ZTILE1']=}")
print(f"{header['ZTILE2']=}")
print(f"{header['ZTILE3']=}")
```
```
header['ZNAXIS1']=2560
header['ZNAXIS2']=1000
header['ZNAXIS3']=1
header['ZTILE1']=256
header['ZTILE2']=256
header['ZTILE3']=1
```

```
# Time loading all the array with astropy
%timeit fits.getdata(path, hdu=1)
75.4 ms ± 597 µs per loop (mean ± std. dev. of 7 runs, 10 loops each)

# Time loading all the array with fitsio
%timeit fio[1][:,:,:]
25.6 ms ± 311 µs per loop (mean ± std. dev. of 7 runs, 10 loops each)

# Time loading a single chunk
%timeit fio[1][0,0,0]
24.6 µs ± 757 ns per loop (mean ± std. dev. of 7 runs, 10,000 loops each)
```

note that opening the file with astropy currently loads the whole array
so takes the same amount of time as the first `getdata` call.

Issue [#3895](https://github.com/astropy/astropy/issues/3895) has been open
since 2015 and describes a set of deep improvements for the compressed image
support in `io.fits`. This includes implementing the compression natively in
Python rather than using the `cfitsio` C library to do it. This will have the
side effect of significantly reducing the compile time complexity of Astropy, as
the bundled cfitsio library could then be removed from the core package (as it
was only used for the compression). We expect that we would address all of the
points in this issue during development of a tile [de]compression package
independent of cfitsio.

Some relevant issues:

* Compressed HDU enhancements [#3895](https://github.com/astropy/astropy/issues/3895)
* Writing compressed FITS files is slow when multi-threaded [#11633](https://github.com/astropy/astropy/issues/11633)
* Refactor FITS compressed image headers (CompImageHeader) [#9238](https://github.com/astropy/astropy/issues/9238)


#### Dask Integration with reading FITS files

While handling compression without loading the whole array is one of the largest
performance issues in `io.fits`, this project is also proposing to increase the
integration of Dask with `io.fits` which will enable significant performance
improvements when using FITS files with dask.

This proposal is focusing on image HDUs in FITS files, so both uncompressed
images and compressed images (which are stored in binary tables underneath), and
proposes to add an option to `io.fits` to read both these types of FITS arrays
directly into Dask arrays.

The proposal team has significant experience with reading various data
formats into Dask arrays, for example FITS images and CASA images and tables.
A proportion of the development time for this section of the proposal will be
devoted to researching the most effective method of loading FITS files into Dask
arrays.

Currently it is
[possible](https://github.com/sunpy/sunpy/issues/2715#issuecomment-413286821)
but not trivial to load an image from a FITS file into a Dask array, via the
"delayed"
functionality in Dask. In this case, the file is opened when reading a chunk of
data from the array, and then closed again afterwards.
This approach works well for a lot of use cases, but is complex, it would be a
lot better if this were integrated into `io.fits` directly. For example, something akin to:

```python
hdulist = fits.open(filepath, use_dask=True)
hdulist[0].data
```
```
dask.array<reshape, shape=(4, 490, 1000, 2560), dtype=float64, chunksize=(1, 1, 1000, 2560), chunktype=numpy.ndarray>
```


For compressed images, Dask integration would allow users to process the
compressed chunks of the image in parallel (either on a single machine or
distributed), as if each compressed tile of the image was a dask chunk then it
can be parallelised over using the various dask schedulers.

This proposal is to get an initial implementation of both of these read use
cases integrated into `io.fits`, and in the process to document any future
improvements that could be made to enhance performance.

### Approximate Budget
