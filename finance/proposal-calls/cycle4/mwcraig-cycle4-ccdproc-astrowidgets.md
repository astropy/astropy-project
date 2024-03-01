### Array API and Visualization


### Project Team
The project team will be Matt Craig. If additional help is needed it will be subcontracted.

### Project Description

There are two pieces to this project, which are essentially independent. One could be funded without funding the other.

1. Implement the Python [array API standard](https://data-apis.org/array-api/latest/) for at least `CCDData` objects, and perhaps `NDData` objects in the core astropy library and in `ccdproc`.
1. Finalize work on a 1.0 release of the `astrowidgets` API and reference implementation.

### Project / Work

#### Array API

Since the bulk of `ccdproc`, `NDData` and `CCDData` were written, there has been a proliferation of array packages beyond `numpy`, which was the single standard array package at the time this coed was originally developed. Adopting the relatively recent [Python array API](https://data-apis.org/array-api/latest/index.html) would enable the use of any of the newer, and in some cases more performant, packages, a list of which is on the [array API site](https://data-apis.org/array-api/latest/purpose_and_scope.html#stakeholders).

As long as a significant rewrite of `ccdproc` is occurring these additional work will be done:

1. Update packaging infrastructure to be `pyproject.toml`-based and add regular wheel builds.
2. Adopt the type of automated code checks that have been adopted by core astropy.
3. Implement a class-based interface as outlined in [this PR](https://github.com/astropy/ccdproc/pull/656).

#### Astrowidgets

The [`astrowidgets`](https://github.com/astropy/astrowidgets) package has been developed in some bursts of activity over the last several years, in part limited by my past availability. This part of the proposal would see the finalization of a "version 1" API and one or more reference implementations. There is a ginga-based implementation already and a bqplot-based implementation is fairly far along. The latter may or may not end up being included in the first stable release of `astrowidgets` depending on the wishes of the other people working on `astrowidgets`.


### Approximate Budget
Currency: US $24,000

This estimate assumes 40 hours/week, $150/hour, for a total equivalent to 4 weeks, though the development effort will be spread over a much longer time span.

The time will be roughly split between the two projects described above.

### Period of Performance

The period of performance is one year from the start of the grant. While this is significantly longer than the amount of time I anticipate these revisions will take, I want to be more realistic than I've been in the past about the overall calendar time needed to complete this work.

My teaching duties are significantly reduced in Fall 2024, which will be my final semester of teaching.
