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
specutils would greatly benefit from the addition of a generic capability for
advanced users to supply their own tailored algorithms (i.e. code) to be used in place of
the defaults. 
We would like to add this capability to specutils, allowing users to apply
advanced analysis and algorithms to specutils spectra via a regularised
interface.  This interface would be analogous to how astroquery provides a
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
   * This framework aims to provide the required interfaces to enable specutils
     to become what IRAF and EsoRex/EsoReflex provide to astronomers: a
     trustworthy environment that aims to reduce the amount of code written by
     individual astronomers, and instead rely on configuration files and short
     code snippets to drive their reduction and analysis pipelines.
   * Such a framework will use our experience in developing
     [PyCPL/PyEsoRex](https://www.eso.org/sci/software/pycpl/)
     around the ESO Pipelines, which allows for interacting with and developing
     recipes in Python, meaning that the pipelines can be easily extended and
     adapted to meet specific science needs, without requiring that astronomers
     become familiar with the intricate details of the pipelines (or require
     that they become numerical analysts tracing sources of error introduce due
     to misuse of numerical algorithms or libraries).
   * This framework also aims to sit in a similar space as other parts of the
     astropy ecosystem, such as the astropy I/O registry abstracting over the
     detecting, reading and writing to files the various astropy classes, or
     astroquery providing a standardised interface to many data providers. In
     the same way that the registry framework lets users get a `Spectrum1D` from
     various files and sources and use it in the same way, this framework would
     abstract over the choice of algorithms and their parameters, meaning that
     users would be able to rapidly switch between different algorithms for
     producing the same result, such as computing the redshift of a galaxy.


1. An example contributed algorithm will be provided, namely a Fast Fourier
Transform (FFT) cross-correlation.  This consists of two steps:

   1. Interpolating the spectra and templates to a common (log) wavelength binning;
   1. Computing the FFTs, inverting the combined result, and shifting the output
      such that it aligns with the redshift bins.

We will adapt existing code developed by our team when porting the MARZ
redshifting code (Hinton et al. 2016, A&C, 15, 61) from Javascript to Python.
The code has been thoroughly tested and validated, addressing the shortcomings
of the original codebase. The choice to implement the FFT code is due to us
being familiar with said codebase, and that there are a large number of
parameters/choices that are available in the algorithm, even though conceptually
the algorithm is quite simple, thereby providing a useful demonstration of how
the framework will operate. For example, being able change which templates
are used in the computation of redshift via a file verses having to modify code
allows for better traceability of results, as well as allowing for more novice
users to be able to provide input into the science.

Whilst such a regularised framework sounds quite heavyweight and burdensome,
that is not what we set out to do. Instead, the framework will aim to be simple
to use, even for quite novice developers and astronomers. The key aspects are
the ability to apply the same algorithm across many spectra, the ability to
run a pipeline with varying choice of parameter on the same spectra, and finally
to keep track of what choices produced a specific result. A python-like
pseudo-code design of what the framework might look like is below:

```
class Algorithm:
    def __init__(self, config):
        # process config, check that parameters are valid, do any initial setup

    def run(self, spec):
        # run the algorithm on a single spectrum, returning a new Spectrum1D

    def run_many(self, spec):
        # run the algorithm across many spectra

    @classmethod
    def read_from_file(self, filename):
        # load the config from a file
        # it would make sense to allow for various config file formats to be
        # supported via the I/O registry

    def write_config(self, filename):
        # write the config to a file

    def new_from_config(self, new_config):
        # create a new instance where the new config replaces the old config
        # would allow replacing specific parameters whilst making the algorithm
        # class effectively immutable
```

And how a user might use the framework in their code:

```
redshifter = Redshifter.read_from_file("myconfig.cfg")
input_dir = Path("input")
output_dir = Path("output")

for filename in inputdir.glob("input/*.fits):
    spec = Spectrum1D.load(filename)
    new_spec = redshifter.run(spec)
    out_filename = output_dir.joinpath(filename.name)
    new_spec.write(out_filename)
```

It would be expected that smaller components would be used to build bigger ones.
For example, raw spectra are not passed immediately to the FFT cross-correlation
algorithm, instead there are a bunch of pre-processing steps (relating to how
lines and the continuum are treated), so you could provide a pre-processing
algorithm, and then wrap the pre-processing algorithm and the FFT
cross-correlation as a single redshifting algorithm.
In many ways, this can be though of as applying a "Configuration-as-Code"
philosophy to science pipelines, trying to make such pipelines more reproducible.

#### Indicative time estimates of each of the phases

1. Framework design/development: 175 hours
2. Adding log-wavelength storage support and FFT cross-correlation across the astropy ecosystem (this will
   touch specutils, ndcube, and astropy, simply because of subclassing, and we
   need to fully test that there is no accidental re-binning or
   re-interpolation, which will require the FFT cross-correlation to be
   developed in parallel): 315
3. Developing fully-worked examples (including notebooks) showing how to use the
   new redshifting algorithm: 140 hours

### Future Work
We are keen to make substantial contributions to specutils in the future.

Some possible projects that could flow on from this work would include:
    * Developing examples of how to use the above framework as part of a
      pipeline using PyEsoRex.
    * Contributing additional new algorithms, or porting over/wrapping existing
      algorithms based on our ESO pipelines and 2dfdr.

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
