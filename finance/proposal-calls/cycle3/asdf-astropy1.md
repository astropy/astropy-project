### Title
 Expanding Astropy and Astropy-affiliated objects to be serialized to ASDF - Part I

### Project Team
- Elizabeth Madison: Approximately 1.5 years of scientific python programming experience; previous experience calibrating HST/WFPC camera and image analysis of resulting orbital data; much experience with image analysis and distortion calibration and projection onto planetary coordinate systems, particularly with regard to Jupiter and Saturn (CV upon request)

- Brett Graham, William Jamieson, Perry Greenfield and Nadia Dencheva will collaborate on this project but will not be funded by this proposal.


### Project Description
The Advanced Scientific Data Format (ASDF) was developed to address shortcomings of the FITS format, like serializing complex WCS transformations or dealing with newer types of instrumentation (IFS, MSA), that FITS is effectively incapable of handling (Thomas, B., Jenness. T. et al. (2015)). A Python library was developed to implement the standard. Extensions to the standard define the schemas (descriptions of how the relevant information should be saved, and used for validation) for astropy types and asdf_astropy is the Python package which serializes astropy types using those extensions.

https://github.com/astropy/asdf-astropy

There is already support for serializing many Astropy objects using ASDF. These include:

- modeling
- coordinate frames (many, but not all frames)
- units and quantities
- tables
- times and dates

https://github.com/asdf-format

Nevertheless, there are a number of other Astropy objects that can benefit from serialization. We propose to implement ASDF serialization for other commonly used astropy types. The work is split in two proposals of which this is the first one. We propose to implement ASDF serialization of

- the remaining coordinate frames
  - frames derived from BaseEclipticFrame
- remaining BaseRADecFrames (LSR, LSRD, LSRK, TETE, TEME)
- the PSF models in photutils

The work includes writing schemas and converters for these data types, writing tests and documentation.


### Approximate Budget
We are requesting $19200 for a salary for the main developer, Elizabeth Madison.

We are submitting a similar second proposal contingent on successful completion of this one.
