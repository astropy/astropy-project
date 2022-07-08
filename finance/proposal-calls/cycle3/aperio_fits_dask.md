### Title
Improve FITS compressed image support and Dask integration in `io.fits`.

### Project Team
Stuart Mumford
Thomas Robitaille
Drew Leonard

### Project Description

This project aims to increase performance of `io.fits` especially around large
compressed image data.

Currently when using tiled FITS compression the Astropy implementation loads
all the tiles into RAM and decompresses them all.
This is highly CPU and memory inefficient, and is one of the reasons Astropy is
significantly slower at loading these types of files than the `cfitsio` package
(which uses the same C library as Astropy for this currently).

While this is one of the largest performance issues in `io.fits`, this project
is also proposing to increase the integration of Dask with `io.fits` which will
enable significant performance improvements when using FITS files with
distributed compute.

It's likely that any significant refactor of `CompImageHDU` will lead to an
implementation not using the `fitsio` C library see
[#3895](https://github.com/astropy/astropy/issues/3895) which also has the side
effect of significantly reducing the compile time complexity of Astropy, as
this is the only part of the code which uses `fitsio`.

Some relevant issues:

* https://github.com/astropy/astropy/issues/3895
* https://github.com/astropy/astropy/issues/11633
* https://github.com/astropy/astropy/issues/9238

### Approximate Budget

Money in return for the sacrifice of sanity required to rework large chunks of
`io.fits`. /s
