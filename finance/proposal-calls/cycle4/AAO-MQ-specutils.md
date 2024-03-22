### Title
Cycle 4 Funding: Realising the full potential of specutils via an extensible
interface for community contributed algorithms

### Project Team
AAO Research Data & Software, Macquarie University  (rds.org.au) 

The foundation of the AAO Research Data & Software (RDS) team is built upon over 
40 years of supporting astronomical observatories in Australia. This software 
development experience ranges from controlling telescopes and their instruments, 
to building data reduction pipelines, to developing and implementing tools that 
store, manage, and analyse data. The RDS team aims to be at the forefront of 
research software and data engineering. We look for the best technology to solve
a problem, but at the same time realise that software is not innovative or useful
if it cannot be maintained, extended, or scaled. We appreciate the benefits that
a holistic view of a software ecosystem can bring, but also recognise that a 
"deep dive" might be necessary to solve a complex problem. And while our historical
strength has an astronomical flavour, our skills and expertise are increasingly 
recognised across research disciplines. Some of our current and recent projects 
include the Data Central Science Platform, including Virtual Observatory services; 
VLT MAVIS Data Reduction pipeline design and development; our state-of-the-art 
Pipelines as a Web Service (PAWS) system; and our recently completed ESO VLT 
Pipelines development and maintenance project.

We propose the following individuals for this project, although other team members 
can be involved if needed:

* James Tocknell
* Anthony Horton
* Brent Miszalski
* Nuria Lorente
* Simon O'Toole

### Project Description
The latest version of specutils includes useful common analysis tasks for
astronomical spectra. 
To realise its potential as a fully-fledged contributor to scientific workflows,
spectutils would greatly benefit from the addition of a generic capability for
advanced users to supply their own tailored algorithms (i.e. code) to be used in place of
the defaults. 
We would like to add this capability to specutils, allowing users to apply
advanced analysis and algorithms to specutils spectra via a regularlised
interface.  This interface would be analagous to how astroquery provides a
regularised interface to access VO and other web services.  It will provide the
opportunity for the community to contribute their own algorithms, e.g. relating
to large community spectroscopic surveys, or other generic methods. This would go
a long way towards providing a sustainable central repository for analysis
algorithms outside of traditional legacy environments (e.g. IRAF).  In this
project we propose implementing the generic interface and will provide an example
implementation of cross-correlation of spectra using Fast Fourier Transforms.

### Project / Work
1. We plan to introduce into specutils a regularised framework for user contributed
algorithms.  We have experience in contributing to specutils loaders, used by
our team to ingest spectra into Data Central.

1. An example contributed algorithm will be provided, namely a Fast Fourier
Transform (FFT) cross-correlation.  This consists of two steps:

   1. Interpolating the spectra and templates to a common (log) wavelength binning;
   1. Computing the FFTs, inverting the combined result, and shifting the output
such that it aligns with the redshift bins.  We will adapt existing code
developed by our team when porting the MARZ redshifting code 
(Hinton et al. 2016, A&C, 15, 61) from Javascript to Python. The code has been
thoroughly tested and validated, addressing the shortcomings of the original codebase.

### Future Work
We are keen to make substantial contributions to specutils in the future.

### Approximate Budget
This funding application is to cover staff time. We estimate 630 hours of effort
are required to complete this project, which at an hourly rate of USD$155/hour
gives a budget of USD$97,650.

#### Minimum useful time

The absolute minimum useful time on this project would be 210 hours, which would
only allow us to implement the FFT-based redshifting. However, no code
templating capability would be included, which undercuts the value of the
redshifting code as an important example of a case study algorithm. Furthermore,
the redshifting code would be a minimal implementation with no integration with
any existing specutils or astropy classes, no support for the conversion to
logspace of templates or spectra as is required by the FFT algorithms. Nor would
there be any time for astronomer-focused documentation, making it hard for
astronomers to use the code. While this very stripped back version may provide
some value, we would strongly suggest that funding the project in its entirety
will give much better value for the astropy project, and for astronomer-users of
specutils.

At the aforementioned rate of USD$155/hour, this would be USD$32,550.

### Period of Performance
We expect the period of performance to be two years.
