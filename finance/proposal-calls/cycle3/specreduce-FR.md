### Title
Continue specreduce (and specutils) development

### Project Team
This is part work by @tepickering and partly an open call to be overseen by Erik Tollerud (@eteq)

### Project Description
This is to continue development that was begun in the previous cycle on building out pieces of specreduce.  Some specific areas that could be tackled by a developer in the coming cycle include:
* ccdproc workflow (i.e., using ccdproc but in a convenient way that feeds into other specreduce steps - either a notebook or a wrapper class)
* Generic manual wavelength calibration classes (i.e. analogs to "identify" from iraf, should use previous specreduce tools for this where possible)
* Automatic wavelength calibration using existing templates (i.e. "reidentify", or "full template" from pypeit)
* flux calibration classes/wrapper functions (note this may be best implemented in specutils, although that requires additional discussion to decide)
* implementation of example notebooks doing the above on real data
* Support for / workflows with multi-object spectrographs
* Continued/expanded outreach to observatories and software projects (e.g. PypeIt) to improve integration and workflows

### Approximate Budget

* @tepickering should be able to allocate $10000 to focus on wavelength calibration, following successful work on the trace object
* Up to $40000 as an open call for a developer to work on any of the other items above.
