## Core/coordinated Package Maintenance and Development

### Project team

This proposal is to fund the following people at [Aperio Software](https://aperiosoftware.com):

* Thomas Robitaille
* Stuart Mumford

This could also fund other individuals working at Aperio Software as required.

### Project Summary

This project covers a number of different areas of work around the Astropy project:

* Maintenance and development of new features in sub-packages in the core astropy package as well as coordinated packages for which Robitaille and Mumford are maintainers
* Contributions to other parts of the core astropy package and coordinated package ecosystem.
* Participation in the release team, including carrying out releases in the core package and working on general infrastructure for releases
* Maintainance and development of the shared OpenAstronomy tooling and infrastructure
* Moderation and support for Slack/Matrix & Discourse.

### Project / work

#### `astropy.io.fits`

This proposal will fund Robitaille for his work co-maintaining `astropy.io.fits`, continuing funding that was awarded to him to start working on this in 2023. The priorities for this work will be:
* Resolving bugs related to the refactoring of the image compression module and work on improving
  performance to be on par or better than the performance of the previous module.
* Continue work on the refactoring of ``CompImageHDU`` to inherit from ``ImageHDU``, and once
  completed, carry out extensive testing with real-world data and code to make sure the new code
  is robust. Once these changes are released to users, address bug reports related to this change.
* Triage and start addressing other existing issues. At the time of writing, there are currently over
  [160 open issues](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Aio.fits) for the io.fits sub-package alone.

#### `astropy.timeseries`

Robitaille will continue co-maintaining the [astropy.timeseries](https://docs.astropy.org/en/stable/visualization/wcsaxes/) sub-package as required. The priorities will be:
* Improving performance and memory usage
* Encouraging adoption in other packages and investigating how the sub-package can be improved to facilitate this
* Exploring how to provide functionality to cater for data cubes with a time axis rather than just plain time series tables.

#### `astropy.visualization.wcsaxes`

Robitaille and Mumford will continue to maintain the [astropy.visualization.wcsaxes](https://docs.astropy.org/en/stable/visualization/wcsaxes/) sub-package, which is used to make plots of a wide range of different data with any APE 14-compliant WCS. The priorities for this sub-package will be:
* Improving performance; very little effort has been made to date to make ``WCSAxes`` as fast as possible, focusing instead on providing good support for APE-14-compliant WCSes. However, there are a number of use cases where performance is becoming a bottleneck (for example in interactive visualizations), so we will focus on profiling and improving performance across the sub-package.
* Fixing issues that have ben reported by users. There are currently over 40 [open issues](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Avisualization.wcsaxes), so we will focus on bringing this number down and improving the stability and reliability of the sub-package overall.

#### reproject

The [reproject](https://github.com/astropy/reproject) coordinated package, implements different image reprojection algorithms. The main areas for future development are:
* Continuing work on integrating the use of [dask](https://www.dask.org) into reproject to improve performance and memory usage when reprojecting large data, and ensure that this can be used for real-world applications of reprojecting and mosaicking larger-than-memory datasets.
* Fixing issues reported by users, in particular ensuring that reproject works properly for state-of-the-art high resolution data (e.g. https://github.com/astropy/reproject/issues/199).
* Exploring other reprojection algorithms that could be integrated into reproject.

#### astropy-healpix

[astropy-healpix](https://github.com/astropy/astropy-healpix) is a stable package which requires minimal maintanance. As part of this proposal we shall continue to triage issues, review pull requests and do releases as needed.

#### Release team

Robitaille is a member of the Astropy project release team, which is responsible for carrying out releases of the core package as well as coordinating release infrastructure across the project. Part of the funding will therefore be used to continue supporting these efforts.

#### OpenAstronomy shared infrastructure

The OpenAstronomy project holds some infrastructure projects shared between Astropy, SunPy and other packages. As part of this proposal we will continue to contribute to and maintain the following projects:
* https://github.com/OpenAstronomy/github-actions-workflows
* https://github.com/OpenAstronomy/build-python-dist
* https://github.com/OpenAstronomy/sphinx-changelog
* https://github.com/OpenAstronomy/publish-wheels-anaconda

This will include collaborating with the Scientific Python project on reducing duplication with their efforts.

#### Participation in general Astropy development

In addition to the specific core sub-packages and coordinated packages mentioned above, we plan to continue contributing in a more general way to the Astropy ecosystem and community. We will respond to issues that we can help with, contribute bug fixes for bugs we encounter or are qualified to fix, help maintain features we have added in the past, participate in developer and other relevant calls when possible, and participate in discussions on the mailing list and in Slack.

#### Moderation and support for Slack/Matrix & Discourse

We will continue to support the administraion and moderation of the Discourse, slack and Matrix community spaces.

### Budget

We request funding to cover 12h/week in total - assuming 48 weeks (to account for holidays!) this gives a total of **USD 86,400 per year** assuming an hourly rate of USD 150/hour. If the budget allows, we would like to request funding for up to three years. If this is not possible, then we would be open to a two year contract. If the budget needs to be reduced further, the minimum useful funding would be to cover 8h/week, which would mean **$57,600 per year**.
