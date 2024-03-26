### Title

Support for Uncertainties, Masks, Improved Quantities, Other Types of Arrays

### Project Team

Marten van Kerkwijk

### Project Description

I request partial buy-out from my professorship at UofT to be able to work one
day a week on projects that are too large for the time I can currently commit
for astropy.  Specifically, I propose,

- To ensure Masked and Distribution can be used in all the main astropy classes
  (Time, Representation, Frame, and SkyCoord).
- Use the new numpy dtype machinery to deal with units, thus speeding up units
  conversions.
- Facilitate Quantity becoming a container class that can handle not just
  ndarray but any type of array, i.e., also dask, jax, etc.
- Extend the same machinery to Masked and Distribution so that all main astropy
  classes can use arbitrary array classes.
- Finish my implementation of a Variable class that tracks uncertainties and
  their correlations analytically (based on the uncertainties package).

### Project / Work

Currently, I spent about a day per week on astropy core, in reviews, bug
fixes, and development.  While I have managed to use extra time for fairly
large developments (Quantity historically and Masked and Uncertainty more
recently, with also fairly major contributions to Time, Table, Representation
and numpy), it has been difficult to find enough time to actually wrap up
larger projects (at least outside sabbaticals).

In particular, while I found time to enable the use of Masked with Quantity
and Time, the logical extension to coordinates is still missing.  Similarly,
Distribution now works well with Quantity, but not with Time and the various
classes underlying coordinates.  Solving this will allow masks and (implicit)
error propagation on all astropy core classes.  Furthermore, an
[PR](https://github.com/astropy/astropy/pull/3715) to introduce a Variable
class that tracks uncertainties and covariances (based on the [uncertainties
package](https://pythonhosted.org/uncertainties/), but extended it to deal
natively with arrays), has been stalled for almost a decade.  All these
require focussed time to finish the implementation, writing tests, documenting
proper usage, etc.

An exciting development at numpy has been the new dtype machinery, which
allows much easier design of user data types.  So far, the main application
has been a new StringDType, which allows having an array of variable-length
unicode strings (I have been a major reviewer of this, partially to get
familiar with the new machinery; it may be useful for astropy too).

One of the explicit use cases for the dtype redesign was to support units
(which can be seen as descriptions of how to interpret the data, with
converting to another unit similar to casting to another data type).  This
seems one of the easiest ways to reduce the intricate dependencies on ndarray
and remove many of the overrides of its methods.  Our unit system itself is
nicely separated out, which should facilitate using it for a new unit-carrying
dtype.  Benefits of using this include speed-up (as much more will be done in
C), and removal of quite tricky code to deal with, e.g., structured data
types.  I also have some hope of separating out the units/quantity code from
astropy, so that it can be used more generally.

Using unit-carrying data types should also make it easier (though is not
required) for Quantity to support other array classes (dask, jax, etc.), as
proposed in [APE 25](https://github.com/astropy/astropy-APEs/pull/91). This
will help deal with larger data sets (dask) or use GPU acceleration(jax).
The [APE 25 report](https://github.com/nstarman/astropy-APEs/blob/units-quantity-2.0/APE25/report.pdf)
lays out in detail how this could work.  My proposal here is to implement it,
write proper tests, ensure there are no performance regressions, and of course
document it all.  A nice benefit of the approach laid out in APE 25 is that it
will be very easy to extend it to Masked and Distribution (and possibly
Variable), as those basically are already the type of container classes that
APE 25 envisions.

A nice things of Quantity being able to use other array types than ndarray is
that this will nearly automatically extend to coordinates (since those use
quantities almost exclusively; I foresee little more work than adjusting
tests!).  Time will be slightly more work, as it works directly with ndarray,
but also here the path is straightforward: I can just follow my earlier work
on ensuring Time can work with Masked.

I should perhaps add that the different projects can be separated relatively
easily, and do not have a very obvious order.  Hence, I can give priority to
whatever is deemed most important.

### Approximate Budget

I request funding to replace salary equivalent to one day a week, reducing my
regular employment at the University of Toronto correspondingly.  At a
standard rate of USD 150/hour (which happens to be roughly my current salary)
for 8 hours per week and 45 weeks, this corresponds to USD $54000 per year.

Note: I have confirmed with my Chair that a reduction, including of teaching,
is possible in principle, but am still in the process of finding out how this
would work in practice.

### Period of Performance

Ideally, this would be for three years (if funding allows and my university
agrees), but the projects are sufficiently separable that a shorter term is
useful too (but not fewer hours per week, since the goal is to have full days
for astropy development only).
