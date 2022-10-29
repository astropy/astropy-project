### Title

### Project Team

Nathaniel Starkman (NS)


### Project Description

Continue role as astropy core maintainer and as the cosmology maintainer,
working to expand cosmology compatibility with 3rd party libraries.

`astropy.cosmology` does not plan to add a Boltzmann code nor other highly
technical domain-specific tools. Many useful 3rd party cosmology codes already
exist, e.g Boltzmann solvers like CLASS, for these purposes. Currently
`astropy.cosmology` has limited-to-no interoperability with these commonly-used
libraries. As maintainer, I will prioritize improving interoperability,
enabling, e.g. someone to create a cosmology instance in Astropy and run on
that cosmology the CLASS Boltzmann solver.


### Project / Work

Continue role as `astropy.cosmology` maintainer:

- Contribute bug fixes and develop new features
- Pull Request reviews and Issue triaging
- Participate as a mentor to new contributors, as a part of a possible formal
  contributor-to-maintainer training program
- Continue developing a roadmap for the subpackage (GitHub Project in progress,
  with ~171 complete and ~141 current, and many more planned)
- Develop new contributed tutorial content on astropy.cosmology

The `astropy.cosmology` package has very few (known) bugs and is mature, so it
receives relatively few Pull Requests and Issues. Consequently, NS anticipates
that interoperability improvements will occupy the majority of the budgeted
time.


Planned interoperability improvements for `astropy.cosmology`:

- Entry-point support to astropy’s Unified I/O, which is in `astropy.io`. NS
  will base this improvement on an existing reference implementation of his.
  Entry-point support in Unified I/O will have use beyond `astropy.cosmology`,
  e.g. allowing 3rd party formats to be available for I/O in `astropy.table`. 
- Prioritize adding I/O support for the following tools: [CLASS]
  (http://class-code.net) and [Colossus]
  (https://bdiemer.bitbucket.io/colossus/cosmology_cosmology.html), adding
  others as time permits.


### Approximate Budget

Target budget: $12,000 for 2 hours/week of work at $120/hour (rate negotiable).
Minimum budget: $6,000 for 2 hours/week of work at $60/hour.

### Approved Budget

$12,000.00.
