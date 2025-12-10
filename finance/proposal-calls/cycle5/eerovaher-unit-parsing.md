### Title

Improving `astropy` unit parsing

### Project Team

Eero Vaher

### Project Description / Scope of Work

Problems in unit parsing can result in problems reading data files, which
complicate or even prevent using `astropy` or coordinated packages to analyze
existing data sets.
One problem that has been known and unsolved for a long time is the poor
support for parsing function units (units involving e.g. log or dex).
Another problem is that in practice many data files contain non-standard units,
so `astropy` should offer options for handling them.
`Unit()` does have the `parse_strict` parameter, which is supposed to control
whether parsing problems should raise an error, emit a warning or be handled
silently, but there are cases where that parameter is simply ignored, for
example parsing deprecated units with `"vounit"` and `"ogip"` formats.
Furthermore, even if users know that a file they want to read contains
non-standard units, they often don't have a good way to define them as custom
units beforehand.

#### Roadmap Items

Parsing function units with the `"fits"` unit format is relevant for

- :red_square: Determine a plan for long-term support of FITS, while also
  improving performance and making contribution easier.

The problems described above are longstanding, so addressing them contributes towards

- :red_square: Identify and ensure progress on longstanding issues that should
  be high priority (e.g., issues in io.votable).

#### Project / Work / Deliverables

The main goals of this project would be:

  - enable support for parsing function units that the unit formats are
    supposed to support,

  - ensure `parse_strict` always does what it claims to do,

  - allow users to explicitly define custom units for use with the `astropy`
    unit parsers.

Past experience suggests that taking a closer look at the `astropy` unit
parsers will reveal both bugs and possibilities for performance improvements.
This proposal also includes general maintenance work on those issues as they
become apparent.

### Approximate Budget

I am proposing to work on this myself 3-5 hours per week for up to 48
weeks and $100 $/hr for a total of $14,400-$24,000.
The lower end of the budget range would allow working on parsing function units
and almost-standard-compliant units, removing surprising behavior from the
`parse_strict` parameter, fixing bugs in the unit parsers and some performance
improvements.
The higher end would additionally allow work on registering custom units and
more performance improvements.

### Period of Performance

Jan 1, 2026–Dec 31, 2026.
