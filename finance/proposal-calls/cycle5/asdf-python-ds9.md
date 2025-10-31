### Title Making DS9 more accessible to ASDF and Python

### Project Team

- Perry Greenfield: Approximately 27 years of scientific python programming
  experience; 50 years of astronomical data reduction experience, 40 years at
  STScI (now retired), former Branch Lead of Science Software Branch;
  involved in all major Python data analysis and calibration projects at
  STScI. Part of the original organizing of astropy. Involved in the creation
  of ASDF (Advanced Scientific Data Format)

### Project Description
The Advanced Scientific Data Format (ASDF) was
developed to address shortcomings of the FITS format, like serializing
complex WCS transformations or dealing with newer types of
instrumentation (IFS, MSA), that FITS is effectively incapable of
handling (Thomas, B., Jenness. T. et al. (2015)). A Python library was
developed to implement the standard. 

Currently astropy makes use of ASDF for serialization of a number of objects,
models, tables and coordinate frames as examples. To help wider adoption of
ASDF by the community, and thus the serialization of astropy objects, it is
important that astronomers have a convenient way of displaying images within
their most used image display tool, namely ds9. Unfortunately STScI is
unwilling to provide such support. I am proposing to add such support to ds9,
as well as making integration of general python tools more easily accessible
from ds9 than they currently are.

The integration will proceed in steps.

1. ds9 provides a means of execution of python code, albeit in a somewhat
awkward manner. Some years past I have developed such a facility for
displaying ASDF images in ds9, though it was never carried through to being
released due to a lack of support from STScI. This first step is to make this
capability available. 

2. The second step is to make the instrinsic ds9 GUI
naturally accept ASDF files as easeily as it uses FITS files. This requires
changes to the internals of ds9, particularly with regard to its user
interface. 

3. ds9 currently only understands FITS WCS information. I plan to
modify it to also work with the python GWCS library. Note the previous steps
bypass this by approximating the GWCS with a SIP fit to the GWCS model).
There is a subtlety that must be dealt with that affects performance since it
will likely be necessary to change the event handling when using GWCS to make
it perform acceptably. 

4. Expand the ds9 interface to allow introspection
within an ASDF file showing where images are located so they can be selected
with the cursor. 

5. The previous steps can be generalized to allow a
mechanism to extend the ds9 interface to handle access to other python
tools.

Since steps 2 and later involve understanding the internals of ds9, it is
difficult to give good estimates of the work involved. This proposal intends
to limit the work to the funds requested. I expect that the first 3 steps
should be achieved; those beyond depend on the difficutly of 2 and 3. This
work also presumes that the current maintainers of ds9 are willing to accept
the required changes for steps 2 and beyond.

### Approximate Budget I am requesting $20,000 to perform this work
    (approximately 133 hours at $150/hr)

### Period of Performance The work will be completed within a year
    (2026-01-01 to 2026-12-31)

