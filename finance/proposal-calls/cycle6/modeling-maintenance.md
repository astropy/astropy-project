### General Maintenance of `astropy.modeling`

**Proposal Category**: Operations

### Project Team
William Jamieson (@WilliamJamieson)

### Project Description / Scope of Work
I currently serve as a maintainer of `astropy.modeling`. However, the time I can
devote to general maintenance is often limited by my other commitments. This
proposal would fund dedicating 5% of my time specifically to the broader needs
of `astropy.modeling`, beyond the work I can take on through my existing project
commitments. This time would support ongoing work that benefits the package and
its wider user community, including issue triage, testing, and targeted
improvements to maintainability and performance.

This work addresses maintenance needs that are important to the long-term health
of the package but may not have an immediate, project-specific deliverable. Some
improvements may also benefit particular scientific projects, but those benefits
cannot always be identified in advance. The funded work would therefore focus on
the needs of `astropy.modeling` as a whole, with priorities guided by user
impact, severity, and the effort needed to deliver reliable changes. It would
support ongoing maintenance, not a time-limited redesign or a commitment to
resolve every open issue.

#### Project / Work / Deliverables

**Issue triage and maintenance**

Review and prioritize issues and pull requests from contributors working on
`astropy.modeling`, as well as changes elsewhere in Astropy that affect it.
Clarify which reports need further investigation, review contributions, and
work on high-impact bugs and other maintenance needs. The goal is to make steady
progress on the backlog while remaining responsive to newly reported problems.

**Testing and reliability**

When addressing modeling issues, I have encountered downstream regressions
because use cases were not covered by tests in `astropy.modeling`. In some
cases, downstream code also relies on behavior that works around an existing
bug. Improve and, where useful, reorganize the test suite to better cover
supported behavior and representative ways users apply `astropy.modeling`, and
to help identify compatibility risks when fixing bugs or changing behavior.
Testing work may also reveal additional bugs to investigate and fix as part of
ongoing maintenance.

**Targeted implementation improvements**

Investigate areas of the core implementation that are unusually difficult to
maintain or cause demonstrated performance problems. Make focused changes where
they can reduce that burden or improve performance, using tests and, where
appropriate, profiling or benchmarks to help verify the changes. This work is
intended to support maintainability—not to undertake a broad rewrite.

Examples of current priorities include [removing the need for a metaclass in
modeling](https://github.com/astropy/astropy/issues/17667) and addressing
[excessive memory use in compound
models](https://github.com/astropy/astropy/issues/16701). These are examples
rather than an exhaustive list; priorities will also be guided by other issues
and maintenance needs that arise during the year.

Progress will be reflected in the resulting issue triage, reviews, tests, bug
fixes, and targeted implementation improvements. The specific work will depend
on the needs and priorities that arise during the period of performance.

### Approximate Budget
Currency: US $

The request is for a sub-award to the Space Telescope Science Institute (STScI)
to fund 5% of my time for the period of performance.

- Sub-award to STScI for 5% effort, including associated costs: $14,109.58
- Travel and conference registration: $1500.00
  This is to help cover the fare, logging, and other fees associated with
  attending one conference or meeting during the period of performance. This
  would be limited to travel within the United States. If requested I am happy
  to provide more specific information when it becomes available.

- **TOTAL: $15,609.58**

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
