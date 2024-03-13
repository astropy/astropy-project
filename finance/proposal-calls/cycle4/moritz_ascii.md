### Title

Addressing issues in `astropy.io.ascii`

### Project Team

- Moritz Guenther (@hamogu)

### Project Description

Address (by fixing or closing) open issues in `astropy.io.ascii`, astropy affiliate editor, organization of dev-telecons, development and review of other astropy and specutils code.


### Project / Work
Part 1: `astropy.io.ascii`
At the time of writing there are [66 open issues in astropy tagged `io.ascii`](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Aio.ascii), 57 of which are older than 18 months.

While astropy clearly thrives with those bugs and issues, each of them represents at least one user
who was stopped in their work and found this annoying enough to open an issue. We know anecdotally, that
many users who do not think of themselves as "developers" don't open issues on github (e.g. they might not 
even have an account) so each bug probably represents several or more users who have run
into a problem. For a smooth user experience, we should close out bugs and fill in feature requests
where we can.

Not all of these issues are actionable (e.g. some 
require upstream fixes or 
[would require fairly invasive changes that would break backwards compatibility in a way that does not seem warrented](https://github.com/astropy/astropy/issues/5440#issuecomment-880703756));
however most can be addressed given some developer time.

Part 2:
Organizational work for Astropy:
- Astropy affiliate package editor with pyOpenSci
- organization of dev-telecons
- strategic planning and proposal writing

Part 3:

Bring X-ray spectroscopy to `specutils` and `astropy.modelling`. Moritz is one of the core developers of [sherpa](https://github.com/sherpa/sherpa/). Sherpa is a complete package for X-ray spectral modelling with an infrastructure very similar to `astropy.modelling`, providing (a) some models and fitters that astropy misses and (b) ways to handle [spectra and responses in the OGIP format](https://heasarc.gsfc.nasa.gov/docs/heasarc/ofwg/docs/spectra/ogip_92_007/node5.html). Indeed, we have made a [bridge between sherpa and astropy a few years ago](https://saba.readthedocs.io/en/latest/), but maintaining compatibility between three separate packages (astropy, saba, sherpa) through versions turned out to be cumbersome. Also, Sherpa has a lot of infrastructure to read OGIP compliant X-ray data (PHA, ARF, RMF) that would fit well into a `specutils.OGIP` package to make those formats available to other parts of the astropy ecosystem. With Sherpa's continued developent in question given NASA's budget proposal to wind down Chandra support, I suggest to move or re-implement (depending on package license) those routines. Several (non affiliated) Python packages have done bits and parts of this, but it seems the time has come to bring the OGIP formats to a well-used astropy ecosystem package like `spectuils`.
Moritz proposes to pay a sub-grant to MIT to pay for some of his time to
work on those issues. Based on previous PRs, I estimate that I can address
on average one issue in one to two work days, so paying for 10% of my work time for one year should allow me to address the majority of the currently open issues.



### Approximate Budget

Budget breakdown (nominal):

- $25,000 for 10% of my time per year

(Since this will be a sub-award to MIT, my salary is fixed by MIT and the overhead rate is fixed by agreement between MIT and the US government. We can change the length of the contract, but not the hourly rate.)

The minimum useful time is determined by how much effort it is to set up that sub-award. I can work on one issue in 8 hours of work, but neither MIT nor NumFOCUS would want to write and process a subaward contract for that little money. Realistically, it's probably not worth the effort if less than $5-10k  are allocated to this project.

### Period of Performance
3 years