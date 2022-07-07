## Infrastructure and core/coordinated package maintenance

### Project team

This proposal is to fund the following people at
[Aperio Software](https://aperiosoftware.com):

* Thomas Robitaille
* Stuart Mumford
* Drew Leonard

This could also fund other individuals working at Aperio Software if needed.

### Project Summary

This project covers three main areas of work:

* Maintenance of project infrastructure (such as pytest and sphinx plugins,
  extension-helpers, continuous integration, wheel building, and so on). As
  illustrated in
  [astropy/astropy-project#118](https://github.com/astropy/astropy-project/issues/118),
  the infrastructure for the project has grown significantly over the last few
  years, and requires regular maintenance.
* Maintenance and development of the
  [astropy.timeseries](https://docs.astropy.org/en/stable/timeseries/) and
  [astropy.visualization.wcsaxes](https://docs.astropy.org/en/stable/visualization/wcsaxes/)
  sub-packages as well as the [reproject](http://reproject.readthedocs.io) and
  [astropy-healpix](https://astropy-healpix.readthedocs.io/en/latest/)
  coordinated packages.

### Project / work

#### Infrastructure work

We will participate in the maintenance of the existing project infrastructure,
which includes:

* pytest plugins and pytest-astropy
* sphinx plugins and sphinx-astropy
* extension-helpers
* auto-release infrastructure (such as the automated building of wheels)
* benchmarks

In addition to fixing issues with these, we will continue to work on trying to
simplify the maintenance burden for the infrastructure by adopting wherever
possible existing technologies and workflows rather than maintaining our own.

We will also work on infrastructure tools being developed under the
OpenAstronomy umbrella which are used by Astropy as well as e.g. Sunpy - this
includes for example workflows for GitHub Actions which are being used in the
Astropy organization.

Finally, we will work on fully developing the integration testing started at
https://github.com/astropy/integration-testing which aims to ultimately
frequently test the interoperability of the whole ecosystem of core and
coordinated packages.

#### astropy.timeseries

The [astropy.timeseries](https://docs.astropy.org/en/stable/timeseries/)
sub-package is currently not very actively maintained, so as part of this
project we will aim to address some of the [open
issues](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Atimeseries)
including both bug fixes and feature requests.

#### astropy.visualization.wcsaxes

We propose to continue maintaining the
[astropy.visualization.wcsaxes](https://docs.astropy.org/en/stable/visualization/wcsaxes/)
sub-package, which is used to make plots of a wide range of different data with
any APE 14-compliant WCS. We will work on some of the [open
issues](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Avisualization.wcsaxes)
as well as new issues that come up, and will also investigate ways of improving
the performance of the plotting.

#### reproject

The [reproject](https://github.com/astropy/reproject) coordinated package, which
implements different image reprojection algorithms, is not very actively
maintained currently. With funding, we will be able to address a number of the
[open issues](https://github.com/astropy/reproject/issues) and carry out new
releases incorporating those fixes. We will work on stabilizing the API with the
goal to release v1.0.0 during this funding cycle.

#### astropy-healpix

Similarly to reproject, the
[astropy-healpix](https://github.com/astropy/astropy-healpix) coordinated
package is in need of maintenance, and also needs some decisions to be made
regarding the API. Once these decisions are resolved, we will target releasing
v1.0.0 of the package during the funding cycle.

### Budget

Project participants will ideally work 16h/week on this project in total -
assuming 48 weeks (to account for holidays!) gives a total of **USD 115,200**
assuming an hourly rate of USD 150/hour. The minimum useful budget to carry out
the work here would be 8h/week in total, which gives a total of **USD 57,600**.
