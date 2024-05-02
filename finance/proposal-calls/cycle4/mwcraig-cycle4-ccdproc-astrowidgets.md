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
3. Implement a class-based interface for image combination as outlined in [this PR](https://github.com/astropy/ccdproc/pull/656).
4. Update code base to remove vestigal code checks and other clean up (e.g. remove a test for whether the user is using astropy `v1.0`)

#### Astrowidgets

The [`astrowidgets`](https://github.com/astropy/astrowidgets) package has been developed in  bursts of activity over the last several years, in part limited by my past availability. This part of the proposal would see the finalization of a "version 1" API and one or more reference implementations. There is a ginga-based implementation already and a bqplot-based implementation is fairly far along. The latter may or may not end up being included in the first stable release of `astrowidgets` depending on the wishes of the other people working on `astrowidgets`.


### Approximate Budget
Currency: US $24,000

This estimate assumes 40 hours/week, $150/hour, for a total equivalent to 4 weeks, though the development effort will be spread over a much longer time span.

A breakdown of the estimated time for each task is below, along with its associated cost. The purpose of this is to make it easier to consider partial funding in the event full funding is not possible.

#### `ccdproc` and `astropy.nddata` work

The items in this section are largely independent of each other and could be funded separately.

Task | Estimated hours | Cost
---- | -------------- | ----
1.a Implement Array API | 35 | $5,250
1.b Update `ccdproc` to use modern packaging and testing | 10  | $1,500
1.c Implement class-based interface for combination | 20 | $3,000
1.d Code clean-up  in `ccdproc`| 10 | $1,500
**SUBTOTAL** | **75** | **$11,250**

#### `astrowidgets` work

The items in this section largely build on each other. If partially funded, it would make sense to provide funding in order (e.g. 2.a and 2.b or 2.a trough 2.d).

Task | Estimated hours | Cost
---- | -------------- | ----
2.a Finalize the stable version of the API and document it   | 35 | $5,250
2.b Split API specification from implementations | 10 | $1,500
2.c Update `ginga`-based implementation to match API | 10 | $1,500
2.d Finish implementation of `bqplot`-based interface | 20 | $3,000
2.e Document the implementations and make sample widgets that build on it | 20 | $3,000
**SUBTOTAL** | **85** | $12,750


### Period of Performance

The period of performance is one year from the start of the grant. While this is significantly longer than the amount of time I anticipate these revisions will take, I want to be more realistic than I've been in the past about the overall calendar time needed to complete this work.

My teaching duties are significantly reduced in Fall 2024, which will be my final semester of teaching.
