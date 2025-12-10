### Title

Quantities with Array API support, Improved Support for Masks and Uncertainties

### Project Team

Marten van Kerkwijk

### Project Description / Scope of Work

I request continued partial buy-out from my professorship at UofT to be able
to work one day a week on projects that are too large for the time I can
otherwise commit for astropy.  Specifically, I propose,

- Facilitate Quantity becoming a container class that can handle not just
  ndarray but any type of array, i.e., also dask, jax, etc.
- Ensure Quantity is fully compliant with the new Quantity API being developped.
- Extend the same machinery to Masked and Distribution so that all main astropy
  classes can use arbitrary array classes.
- Also extend the machinery to the internal arrays used by Time.
- Speed up unit conversion and thus all of astropy by smarter conversion
  functions and caching.
- Finish my implementation of a Variable class that tracks uncertainties and
  their correlations analytically (based on the uncertainties package).

#### Roadmap Items

I split these into direct goals of my work and pieces that will be enabled by
it.  Here, note that my goal of adding quantity support for non-numpy arrays
includes support for JAX and Dask arrays, which would thus provide a major
requirement for astropy as a whole having support for those.

Directly addressed:

- :green_circle: Add quantity support for non-NumPy arrays.

- :large_orange_diamond: Improve interoperability between unit packages (e.g.,
  `astropy.units`, `pint`, `unyt`).

Provides a major requirement for:

- :red_square: Support JIT compilation (e.g., numba, JAX, etc.) throughout
  Astropy core and coordinated packages.

- :large_orange_diamond: Improve and/or maintain interoperability with
  performant I/O file formats and libraries such as HDF5 and Dask.

#### Project / Work / Deliverables

Prior to cycle 4, I spent about a day per week on astropy core, in reviews,
bug fixes, and development.  I managed to use extra time for fairly large
developments (Quantity historically and Masked and Uncertainty more recently,
with also fairly major contributions to Time, Table, Representation and
numpy), but it was difficult to find enough time to actually wrap up larger
projects (at least outside sabbaticals).  This changed with cycle 4 funding,
and a major part of this request is to complete some of the main parts of the
project I proposed for that cycle.

In particular, in the current cycle I have started to develop Quantity 2.0.
As proposed in [APE 25](https://github.com/astropy/astropy-APEs/pull/91), this
follows the [Array API](https://data-apis.org/array-api/), ensuring
that the new Quantity class will work with any array that supports that API,
which includes those that really matter, like Dask for large, disk-based data
sets and JAX for GPU acceleration.  There is a
[prototype](https://github.com/astropy/quantity-2.0), which already supports a
large part of the Array API (basically, those provided by numpy ufuncs) for JAX
and Dask.  The work has been waylaid a little in a good way: during this period,
serious discussions started between the various units packages about a shared
[Quantity API](https://github.com/quantity-dev), which we would of course want
to follow.

The primary goal of my proposal here is to finish the implementation, make it
compatible with the new Quantity API, ensure there are no performance
regressions, and of course document it all.

A nice benefit of the approach laid out in
[APE 25](https://github.com/astropy/astropy-APEs/pull/91) is that it will be
very easy to extend it to Masked and Distribution (and possibly Variable), as
those basically are already the type of container classes that APE 25
envisions.

Furthermore, a direct benefit of Quantity being able to use other array types
than ndarray is that this will nearly automatically extend to coordinates
(since those use quantities almost exclusively; I foresee little more work
than adjusting tests!).  Time will be slightly more work, as it works directly
with ndarray, but also here the path is straightforward: I can just follow my
earlier work on ensuring Time can work with Masked.

Most of the above would benefit application of astropy on large arrays, by
allowing disk-based ones, and analysis via GPUs.  But astropy is often used on
small arrays too, and while reviewing our own Quantity code as well as the
code for ndarray that it relies on, I realized there are a number of ways in
which we can improve the performance of Quantity and Unit operations for
scalars and small arrays, mostly by reducing overhead.  Some initial PRs on
the numpy side add a [fast path for
scalars](https://github.com/numpy/numpy/pull/29819) and [include array storage
in the object](https://github.com/numpy/numpy/pull/29878).  On the Quantity
side proper, I have a skeleton of code that would make unit conversion
substantially faster, especially if combined with caching.  This would again
mostly benefit small arrays.  Also for larger ones, I see a nice path forward:
the new dtype machinery of numpy provides a way to do the scaling needed for
unit conversion as part of an operation, thus avoiding the need to create
large temporary arrays.

Finally, an undergraduate I was taught that a number without a unit or an
uncertainty is meaningless.  Quantity provides the former, and Distribution
provides a monto-carlo like method for the latter.  But often we just would
like to have error propagation, but including covariance.  More than a decade
ago, I made a [PR](https://github.com/astropy/astropy/pull/3715) to introduce
a Variable class that tracks uncertainties and covariances (based on the
[uncertainties package](https://pythonhosted.org/uncertainties/), but extended
it to deal natively with arrays).  This has been stalled since, but I believe
would still be super useful.  A stretch goal of the current proposal is to
finally finish it.

### Approximate Budget

I request funding to replace salary equivalent to one day a week, reducing my
regular employment at the University of Toronto correspondingly.  At a
standard rate of USD 150/hour for 8 hours per week and 45 weeks, this
corresponds to USD $54,000 per year.

I note that my initial cycle 4 proposal was for three years, but that made it
extend beyond the cycle 4 funding cycle and hence the initial allocation was
for two years.  With the cycle changing, so far only 16 months have been used.
Here, I request funding both to complete the two years previously approved
($36,000), and in addition request funding for the third year required to
finish the project ($54,000). The total request is thus $90,000.

Given partial funding, I could do:

- $36,000 (remainder approved in cycle 4): Wrap up making Quantity a container
  class compliant with Array API; implement some of the performance
  improvements in unit conversion.

- $72,000 (above plus minimum amount to get partial teaching relief): Produce
  a Quantity replacement without performance regressions, fully integrated in
  astropy (i.e., usable inside SkyCoord, etc.), and fully compliant with the
  Quantity API; implement full set of performance improvements in units
  conversion; probably able to ensure Masked can also hold arbitrary Array API
  compatible arrays, and possibly Time as well.

- $90,000 (full request): Ensure Masked, Distribution, and Time all can hold
  arbitray Array API compatiblle arrays, making astropy as a whole able to
  deal with JAX, dask, etc., arrays.  Hopefully also produce a properly
  functioning Variable class.

### Period of Performance

Ideally, I would be covered until June 2027, which is the end of an academic
year.

I note that the funding provides me with teaching relief for one semester of
an academic year. During those semesters I spend more than 1 day/week on
astropy, while I spend less time when I teach.  The first semester I had
teaching relief was July-December 2024, and the second will be January-June
2026 (some of which will thus be covered by funds already paid). I think it
will be possible to ensure the next semester will be July-December 2026, so
that most work is finished in 2026.
