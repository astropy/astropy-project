### X-ray spectroscopy and `io.ascii` fixes

### Project Team

- Moritz Guenther (@hamogu)

### Project Description / Scope of Work

Address (by fixing or closing) open issues in `astropy.io.ascii`, astropy affiliate editor, organization of dev-telecons, development and review of other astropy and specutils code.

**Relations to cycle 4 request**: In [the discussion on Moritz cycle 4 request](https://github.com/astropy/astropy-project/pull/385#issuecomment-1989445025) the finance committee requested a 2-3 year budget and a matching scope; this proposal is to execute year 2 of that longer-term plan. Work has [started](https://github.com/astropy/astropy-project/issues/405) but delayed transfer of the funding from NumFOCUS to MIT and medical leave for Moritz in the fall of 2025 mean that only a fraction of the originally proposed work has been done so far (but more will be done before the end of the year)

#### Roadmap Items

In addition to bug-fixing and ongoing maintenance, this proposal will address the following [roadmap items](https://github.com/astropy/astropy-project/blob/main/roadmap/roadmap.md):

- Provide next-generation spectroscopic analysis tools usable by individual researchers and larger surveys. (**in this proposal**: X-ray data and X-ray surveys)
- Improve support and validation for input/output (I/O) of standard and user-defined file formats used in astronomy by improving the unified I/O system. (**in this proposal**: [NASA OGIP formats](https://heasarc.gsfc.nasa.gov/docs/heasarc/ofwg/docs/spectra/ogip_92_007/ogip_92_007.html) for PHA, ARF, and RMF files - standard formats for spectroscopy in X-rays)

Both items are marked green in the roadmap, but the existing team works for optical.IR data. This proposal addresses the same items **for X-ray spectroscopy**.

#### Project / Work / Deliverables
##### Part 1: `astropy.io.ascii`
At the time of writing there are [> 50 open issues in astropy tagged `io.ascii`](https://github.com/astropy/astropy/issues?q=is%3Aopen+is%3Aissue+label%3Aio.ascii).

While astropy clearly thrives with those bugs and issues, each of them represents at least one user
who was stopped in their work and found this annoying enough to open an issue. We know anecdotally, that
many users who do not think of themselves as "developers" don't open issues on github (e.g. they might not 
even have an account) so each bug probably represents several or more users who have run
into a problem. For a smooth user experience, we should close out bugs and fill in feature requests
where we can.

Work continues as part of cycle 4 funding (https://github.com/astropy/astropy-project/issues/405) to address those, but funding in cycle 4 is insufficient ot address all of them.

**Deliverable**: Close 20 issues older than 18 months, at least half of which require new code or docs (others may be closed as "won't fix" or turn out to be not relevant any longer)

##### Part 2:
Organizational work for Astropy

**Deliverables**:
- Act as Astropy affiliate package editor with pyOpenSci
- Organization of dev-telecons


##### Part 3:

Bring X-ray spectroscopy to `specutils` and `astropy.modelling`. Moritz is one of the core developers of [sherpa](https://github.com/sherpa/sherpa/). Sherpa is a complete package for X-ray spectral modelling with an infrastructure very similar to `astropy.modelling`, providing (a) some models and fitters that astropy misses and (b) ways to handle [spectra and responses in the OGIP format](https://heasarc.gsfc.nasa.gov/docs/heasarc/ofwg/docs/spectra/ogip_92_007/node5.html). Indeed, we have made a [bridge between sherpa and astropy a few years ago](https://saba.readthedocs.io/en/latest/), but maintaining compatibility between three separate packages (astropy, saba, sherpa) through versions turned out to be cumbersome. Also, Sherpa has a lot of infrastructure to read OGIP compliant X-ray data (PHA, ARF, RMF) that would fit well into a `specutils.OGIP` package to make those formats available to other parts of the astropy ecosystem. With Sherpa's continued developent in question given NASA's budget proposal to wind down Chandra support, I suggest to move or re-implement (depending on package license) those routines. Several (non affiliated) Python packages have done bits and parts of this, but it seems the time has come to bring the OGIP formats to a well-used astropy ecosystem package like `spectuils`.

**Deliverable**: Implement reading of OGIP PHA, ARF, RMF files into `specutils`, and ARF and RMF forward folding as a model in `astropy.modelling` or `specutils`.

### Approximate Budget
Budget breakdown (nominal):

- $30,000 for 10% of my time per year

(Since this will be a sub-award to MIT, my salary is fixed by MIT and the overhead rate is fixed by agreement between MIT and the US government for NASA grants. We can choose the amount of time funded, but not the hourly rate.)

The minimum useful time is determined by how much effort it is to set up that sub-award. I can work on one issue in 8 hours of work, but neither MIT nor NumFOCUS would want to write and process a subaward contract for that little money. Realistically, any award below $10k is probably not worth the effort.

### Period of Performance

Jan 1, 2026–Dec 31, 2026 would work (flexible).