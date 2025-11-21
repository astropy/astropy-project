## Core/coordinated Package Maintenance and Development

### Project team

This proposal is to fund the following people at [Aperio Software](https://aperiosoftware.com):

* Thomas Robitaille
* Stuart Mumford

This could also fund other individuals working at Aperio Software if required.

### Project Description / Scope of Work

This project covers work in the following areas:

* Maintenance and development of new features in sub-packages in the core astropy package as well as coordinated packages for which Robitaille and Mumford are maintainers
* Contributions to other parts of the core astropy package and coordinated package ecosystem.

#### Roadmap Items

This work would go towards the following roadmap items:

- :red_square: Determine a plan for long-term support of FITS, while also improving performance and making contribution easier.

as well as the following for the core package sub-packages and coordinated packages for which Robitaille and/or Mumford are maintainers:

- :red_square: Identify and ensure progress on longstanding issues that should be high priority (e.g., issues in io.votable).

Work will also be carried out towards resolving the following roadmap item:

- :large_orange_diamond: Improve and/or maintain interoperability with performant I/O file formats and libraries such as HDF5 and Dask.

in particular in astropy.io.fits and reproject.

#### Project / Work / Deliverables

#### `astropy.io.fits`

This proposal will fund Robitaille for his work co-maintaining `astropy.io.fits`. The priorities for this work will be triaging issues to identify the highest priority ones and starting to address some of them. At the time of writing, there are currently over
  [150 open issues](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Aio.fits) for the io.fits sub-package alone. In addition to this work, Robitaille will coordinate with other io.fits maintainers to start designing a long-term plan for modernizing the io.fits sub-package and facilitating long-term maintenance and contributions.

#### `astropy.timeseries`

Robitaille will continue co-maintaining the [astropy.timeseries](https://docs.astropy.org/en/stable/visualization/wcsaxes/) sub-package as required. The priorities will be:
* Improving performance and memory usage
* Encouraging adoption in other packages and investigating how the sub-package can be improved to facilitate this
* Exploring how to provide functionality to cater for data cubes with a time axis rather than just plain time series tables.

#### `astropy.visualization.wcsaxes`

Robitaille and Mumford will continue to maintain the [astropy.visualization.wcsaxes](https://docs.astropy.org/en/stable/visualization/wcsaxes/) sub-package, which is used to make plots of a wide range of different data with any APE 14-compliant WCS. The priorities for this sub-package will be:
* Improving performance; very little effort has been made to date to make ``WCSAxes`` as fast as possible, focusing instead on providing good support for APE-14-compliant WCSes. However, there are a number of use cases where performance is becoming a bottleneck (for example in interactive visualizations), so we will focus on profiling and improving performance across the sub-package.
* Fixing issues that have ben reported by users. There are currently over 48 [open issues](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Avisualization.wcsaxes), so we will triage these issues to identify the highest priority ones and start addressing them.

#### reproject

The [reproject](https://github.com/astropy/reproject) coordinated package, implements different image reprojection algorithms. The main areas for future development are:
* Continuing work on integrating the use of [dask](https://www.dask.org) into reproject to improve performance and memory usage when reprojecting large data, and ensure that this can be used for real-world applications of reprojecting and mosaicking larger-than-memory datasets.
* Fixing issues reported by users, in particular ensuring that reproject works properly for state-of-the-art high resolution data (e.g. https://github.com/astropy/reproject/issues/199).
* Exploring other reprojection algorithms that could be integrated into reproject.

#### astropy-healpix

[astropy-healpix](https://github.com/astropy/astropy-healpix) is a stable package which requires minimal maintanance. As part of this proposal we shall continue to triage issues, review pull requests and do releases as needed.

#### Participation in general Astropy development

In addition to the specific core sub-packages and coordinated packages mentioned above, we plan to continue contributing in a more general way to the Astropy ecosystem and community. We will respond to issues that we can help with, contribute bug fixes for bugs we encounter or are qualified to fix, help maintain features we have added in the past, participate in developer and other relevant calls when possible, and participate in discussions on the mailing list and in Slack.

### Approximate Budget

The budget consists of two main parts:

* Funding to cover the existing Cycle 4 extension contract which is being
  charged to ROSES24. This contract was intended to cover previously approved
  Cycle 4 funding which was not all spent by the end of the original contract.
  The total amount for this portion is **USD 58,600**. More than half of this
  amount has already been invoiced for work carried out, and the remainder will
  likely be used by the end of 2025.

* New funding to cover 8h/week in total in 2026 - assuming 48 weeks (to account
  for holidays!) this gives a total of **USD 57,600** assuming an hourly rate of
  USD 150/hour.

The total amount requested is **USD 116,200**.

If funding was limited, we still request **USD 58,600** of already approved/contracted funds, but could reduce the new funding request to 4h/week (**USD 28,800**), for a total of **USD 87400**.

### Period of Performance

Mar 1, 2025 to Dec 31, 2026
