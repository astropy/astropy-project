### Title

`astropy` code quality maintenance by Eero Vaher

### Project Team

Eero Vaher

### Project Description

`astropy` is a large project with a long history, which means it has had to
ensure compatibility with many different versions of the Python programming
language and dependencies such as NumPy.
Opportunities for improving `astropy` code become available both because of
updates to `astropy` itself, but also because `astropy` does not have to
maintain compatibility with old enough versions of its dependencies.
Higher code quality can be beneficial for developers actively working on the
code, but in some cases it can also benefit users by leading to performance
improvements.
However, finding code that could benefit from being updated can be difficult
because such code often does not cause any obvious failures, so dedicated and
on-going effort is required to identify and improve it.

The work I am proposing would be in addition to the normal maintenance work and
pull request reviews expected from an `astropy` sub-package maintainer.

### Project / Work

More specific examples of tasks that improve `astropy` code quality and that I
hope to continue working on include:

- Making use of new features of the Python language and its standard library
  that might not have been available when `astropy` code was originally
  written.
- Making use of new features implemented in Python packages `astropy` depends
  on or in `astropy` itself.
- Identifying and removing compatibility code for obsolete versions of
  dependencies.
- Identifying `astropy` code that is not tested at all or poorly tested and
  improving test coverage accordingly.
- Helping maintain configuration for Ruff linter and formatter to prevent
  code quality regressions.

### Approximate Budget

I am requesting $120/hour for 8 hours per week and 48 weeks per year, amounting
to $46,080 per year. The minimum useful funding would be for 4 hours per week,
amounting to $23,040 per year.

### Period of Performance

I request funding for the maximum possible duration starting from January 2025.
