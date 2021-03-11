### Title

Enhancements to gala and improved interoperability with other Astropy affiliated
packages


### Project team

Adrian Price-Whelan


### Project Summary

[Gala](https://gala.adrian.pw) is one of two specialized Galactic dynamics
Astropy affiliated packages (with [Galpy](https://docs.galpy.org/)). Community
consensus is that having two packages is beneficial to the community, as they
naturally provide validation and checks on one another for implementations of
detailed dynamical machinery. However, users who use both packages have
requested to have enhanced interoperability between the packages. This proposal
aims to fund a developer (the *developer*), mentored by the proposer (@adrn), to
firstly improve interoperability between these two packages. Upon completion of
this work, the *developer* would then work on improving interoperability between
gala and other dynamics community tools like AMUSE and Agama (not yet Astropy
affiliated packages). Once this work is completed, the *developer* will have
been introduced to much of the internals of gala: The third work package will
leverage this expertise to work on new development within Gala.


### Project / work

**Work package 1 (interoperability)**: Review and improve interoperability
between Gala and Galpy

The *developer* will first learn how to perform some core tasks in both
[Gala](https://gala.adrian.pw) and [Galpy](https://docs.galpy.org/), such as
numerically integrating an orbit, defining gravitational potential objects, and
analyzing/manipulating orbit objects. The *proposer* will work closely with the
*developer* to review places where improved interoperability would benefit
users, starting with a few key,
previously-identified pieces of functionality:

- Export and import orbits and phase-space coordinate instances to/from Galpy
- Export and import potential instances to/from Galpy

This feature request has already been identified and tracked in [Gala Issue
194](https://github.com/adrn/gala/issues/194).

Estimated effort: 30 hours

**Work package 2 (interoperability)**: AMUSE and Agama representations of gala
potentials

[AMUSE](https://amuse.readthedocs.io/) and [Agama](http://agama.software/) are
two other dynamics- or simulation-focused packages that are used heavily in
Galactic dynamics research. Using the list of interoperability points defined
for Gala and Galpy, the *developer* will then implement interfaces to enable
interoperability with AMUSE and Agama.

This feature request has already been identified and tracked in [Gala Issue
210](https://github.com/adrn/gala/issues/210).

Estimated effort: 20 hours

**Work package 3 (new development)**: Enhancements to the Potential classes

After implementing WP's 1 and 2, the *developer* will have experience working
with and modifying the internal functionality in Gala. The final work package
will leverage this experience and knowledge to fund the *developer* to implement
long-requested new features in Gala. In particular, several key new features
have been requested to improve the existing Potential classes in Gala:

- Enable time-dependent parameters [Gala Issue
  153](https://github.com/adrn/gala/issues/153) (60 hours)
- Support passing time information to analysis methods [Gala Issue
  66](https://github.com/adrn/gala/issues/66) (10 hours)
- Enable potentials to understand coordinate symmetries to simplify input for
  analysis methods [Gala Issue 39](https://github.com/adrn/gala/issues/39) (30
  hours)

Estimated effort: 100 hours

### Budget

The total budget request for development is estimated based on a $150/hour rate
for 150 hours ($22,500).

The budget also includes funding for a AAS job register ad to remain active for
8 weeks (at $71.84 per week).

| Item | Requested Amount |
|--------|--------|
|   AAS job ad | $575 |
|   WP1 | $4,500 |
|   WP2 | $3,000 |
|   WP3 | $15,000 |
| **TOTAL**     | **$23,075** |

As this proposal contains several self-contained work packages, I also define a
minimum requested budget which eliminates WP2 and some components of WP3.

| Item | Minimum Requested Amount |
|--------|--------|
|   AAS job ad | $575 |
|   WP1 | $4,500 |
|   WP3 (partial) | $9,000 |
| **TOTAL**     | **$14,075** |
