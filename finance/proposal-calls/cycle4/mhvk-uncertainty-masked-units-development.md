### Title

Support for Uncertainties, Masks, Improved Quantities, Other Types of Arrays

### Project Team

Marten van Kerkwijk

### Project Description

I request partial buy-out from my professorship at UofT to be able to work one
day a week on projects that are too large for the time I can currently commit
for astropy.  Specifically, I propose,

- To enhance Masked and Distribution such that they can be used in all the
  main astropy classes (Time, Representation, Frame, and SkyCoord).
- Use the new numpy dtype machinery to deal with units, thus speeding up units
  conversions and facilitating Quantity becoming a container class that can
  handle not just ndarray but any type of array, i.e., also dask, jax, etc.
- Extend the same machinery to Masked and Distribution so that all main astropy
  classes can use arbitrary array classes.
- Introduce a new Variable class that tracks uncertainties and their correlations
  analytically (based on ideas from the uncertainties package).

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
error propagation on all astropy core classes.  Furthermore, an attempt to
introduce a Variable class that tracks uncertainties and covariances has been
stalled for almost a decade.  All these require focussed time.

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
suggested in APE 25. This will help deal with larger data sets (dask) and gain
us GPU acceleration (jax).  The nice things is that if Quantity is able to use
other array types than ndarray, then this will nearly automatically extend to
coordinates (since those use quantities almost exclusively). A bit more of an
obstacle will be Time, though there a user dtype to hold the two parts of the
JD (or indeed a proper quad-precision float) may help similarly: make the
implementation a lot cleaner, and allow other array types than ndarray.  Also,
once Quantity is done, it will be easy to extend it to Masked and Distribution
(and possibly Variable), as those are basically container classes already.

I should perhaps add that the different projects can be separated relatively
easily, and do not have a very obvious order.  Hence, I can give priority to
whatever is deemed most important.

### Approximate Budget

I request funding to replace salary equivalent to one day a week, reducing my
regular employment at the University of Toronto correspondingly.  At a
standard rate of USD 150/hour (which happens to be roughly my current salary)
for 8 hours per week and 45 weeks, this corresponds to USD $54000 per year.

Note: so far I have done nothing beyond asking my Chair whether a reduction,
including of teaching, might be possible in principle.  I will ask for details
if this proposal is deemed interesting.

### Period of Performance

Ideally, this would be for three years (if funding allows and my university
agrees), but the projects are sufficiently separable that a shorter term or
one split in, say, half-year parts is useful too (but not fewer hours per
week, since the goal is to have full days for astropy development only).
