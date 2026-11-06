### Measure and improve I/O performance in astropy

**Proposal Category**: Innovations

### Project Team

This proposal is to fund the following people at [Aperio Software](https://aperiosoftware.com):

* Thomas Robitaille
* Stuart Mumford

This could also fund other individuals working at Aperio Software if required.

### Project Description / Scope of Work

The goal of this project is to measure and improve performance for reading and writing files in different formats with astropy.

#### High Priority Objectives

This work will directly address objective [O7](https://astropy-roadmap.readthedocs.io/en/latest/#o7-improve-and-maintain-interoperability-with-performant-i-o-file-formats-and-libraries) of the Astropy roadmap (Improve and maintain interoperability with performant I/O file formats and libraries), and we aim to complete all three key results:

* **KR7.1** Benchmarks in astropy-benchmarks measure time and peak memory for reading and writing full files and for reading subsets of data, at small and large (≥1 GB) file sizes, for tabular and raster data formats

* **KR7.2** Equivalent reference benchmarks exist for other Python libraries where relevant (e.g. fitsio, h5py, pyarrow, asdf), and tracking issues (one per format) list every case where astropy is more than 2x worse in time or peak memory

* **KR7.3** At least five of the cases in the KR7.2 tracking issues (or all, if fewer than five) are brought within 2x of the reference benchmark through work on Astropy ecosystem packages

#### Project / Work / Deliverables

We will start off by assessing what benchmarks already exist in [astropy/astropy-benchmarks](https://github.com/astropy/astropy-benchmarks) and identifying any gaps for the following:

* FITS, HDF5, VOTable, Parquet, VO-Parquet and ASDF for tabular data
* FITS, including both uncompressed and tile-compressed images, for raster data

We will then add benchmarks as needed to cover all of these, as well as comparison benchmarks with third-party libraries (e.g. [fitsio](https://github.com/esheldon/fitsio)), either in astropy-benchmarks or in a separate repository (since these may not conceptually fit into astropy-benchmarks).

At this point, we will open a tracking issue for each format, summarizing the benchmarks where performance is significantly worse in astropy (using a factor of 2 as a threshold, as specified in the objective). We will then work on addressing as many of these as possible with the remaining funding, aiming to complete **KR7.3** by addressing at least five of the cases.

### Approximate Budget

120h @ USD 150/hour = USD 18,000

### Period of Performance

Jan 1, 2027 – Dec 31, 2027.
