# Astropy ecosystem integration testing

### Project team

The project has to have the consensus from the infrastructure team, then the implementation will be carried out by:

* Brigitta Sipőcz

### Project Summary
Automated system for integration testing of astropy core and the the astropy coordinated and infrastructure packages

### Project / work:

A currently missing procedural element in the ecosystem is a robust
way of testing the compatibility and interoperability of packages. 
The current way of how continuous integration is used is limited 
towards testing with a matrix of version combinations of upstream 
dependencies. However, even if downstream packages routinely run 
tests using the latest development version of, e.g. astropy, the 
feedback cycle from these downstream users is not automated. 
Capturing regressions early, during the development cycle can 
prevent bugs from being released. As part of this project, I will 
lead the efforts of setting up a community (e.g. the infrastructure 
team) accepted policy and implementing a solution for integration 
testing through the ecosystem of astropy coordinated and 
infrastructure packages. The primary challenge for such a system 
will be to find the balance in the feedback loop whether reports 
should be issued upstream to the astropy package or even to Numpy 
or Python; or downstream, to the packages using astropy. This is a 
critical element in policymaking, as reporting all downstream 
failures has the counterproductive effect of overwhelming upstream 
maintainers with irrelevant reports. 

Potential beyond astropy: Once a solution is implemented for the 
Astropy project, I could coordinate with project leads of packages 
in the broader scientific Python ecosystem advocating for the 
adoption of the same or similar system.

### Budget

Coordinating, implementing, and maintenance of the project is 
estimated to require an average of 2h/week effort. Assuming 48 
weeks  gives a total of **USD
14400** with an hourly rate of USD 150/hour.
