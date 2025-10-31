### Expanding Astropy and Astropy-affiliated objects to be serialized to ASDF

### Project Team
- Perry Greenfield: Approximately 27 years of scientific python programming
experience; 50 years of astronomical data reduction experience, 40 years at
STScI (now retired), former Branch Lead of Science Software Branch; involved
in all major Python data analysis and calibration projects at STScI. Part of
the original organizing of astropy. Involved in the creation of ASDF (Advanced
Scientific Data Format).
- Nadia Dencheva: Approximately 25 years of scientific python programming
experience; Currently at STScI but will be retired by the time work starts
on this proposal. Previous Science Calibration Software Branch Manager; 25
years at STScI; primary author of Generalized World Coordinate System package
and general expert on World Coordinate Systems and ASDF.

### Project Description / Scope of Work
The Advanced Scientific Data Format (ASDF) wasdeveloped to address shortcomings
of the FITS format, like serializing complex WCS transformations or dealing with
newer types of instrumentation (IFS, MSA), that FITS is effectively incapable of
handling (Thomas, B., Jenness. T. et al. (2015)). A Python library was developed
to implement the standard. Extensions to the standard define the schemas
(descriptions of how the relevant information should be saved, and used for
validation) for astropy types and asdf_astropy is the Python package which
serializes astropy types using those extensions.

https://github.com/astropy/asdf-astropy

There is already support for serializing many Astropy objects using ASDF.
These include:

- modeling
- coordinate frames (many, but not all frames)
- units and quantities
- tables
- times and dates

Nevertheless, there are a number of other Astropy objects that can benefit
from serialization. We propose to implement ASDF serialization for other
commonly used astropy types. We propose to implement ASDF serialization of

- the remaining coordinate frames
   - frames derived from BaseEclipticFrame
   - remaining BaseRADecFrames (LSR, LSRD, LSRK, TETE, TEME)
- photutil PSF models (AiryDiskPSF, CircularGaussianPRF,
CircularGaussianPSF, GaussianPRF, GaussianPSF, MoffatPSF, GriddedPSFModel)
- photutil apertures (pixel and sky)
- regions

The work includes writing schemas and converters for these data types,
writing tests and documentation. Some of these items were part of an accepted
Cycle 4 proposal, but the work was truncated early due to the developer not
making sufficient progress, and a relatively small amount of money was expended.
The current developers both have extensive experience writing schemas and
converters as part of their previous work.

#### Project / Work / Deliverables

The above listed astropy objects will be serialized as part of asdf-astropy.

### Approximate Budget
We are requesting $20,000 (approximately 133 hours at $150/hr) for the
salaries for the two developers:Perry Greenfield and Nadia Dencheva, who
will no have any competing professional demands on their available time.

### Period of Performance
The work will be completed within a year (2026-01-01 to 2026-12-31)
