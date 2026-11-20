### Spectroscopy Development

**Proposal Category**: Innovations

### Project Team
Timothy Pickering

### Project Description / Scope of Work
This a continuation of spectroscopy development and outreach carried out in previous cycles as well tackling two spectroscopy-related high-priority objectives.

#### High Priority Objectives
- Add read/write support for the IVOA SpectrumDM format to `specutils`. This proposal will address and complete the following key results from the Astropy roadmap:
    - **KR8.1**: `specutils` reader for SpectrumDM-compatible `VOTables`, including tests and test data from at least two different archives.
    - **KR8.2**: `specutils` writer that can write a `Spectrum` object to a SpectrumDM `VOTable` that passes `astropy`'s `VOTable` validator and includes all fields that SpectrumDM marks as mandatory.
    - **KR8.3**: Reading and writing as in KR8.1 and KR8.2 via the SpectrumDM FITS serialization (including validation), demonstrated with at least one archive-provided file.
- Begin the work of supporting the `Array` interface protocol in `specreduce`. This ties into both the work being done to make `Quanitity` `Array` compliant as well as improving interoperability with performant I/O file formats and libraries that `Array` would facilitate. This work directly addresses the following key result from the Astropy roadmap:
    - **KR1.2**: With a backward-compatibility layer in place, the existing test suites of astropy core and all coordinated packages, including `specreduce`, pass with no new failures against the new Quantity.

#### Project / Work / Deliverables
- A SpectrumDM reader/writer should be a relatively straightforward deliverable. The documentation is all there, but examples of real-world data will need to be collected for testing.

- The `ccdproc` package has begun work on supporting `Array` so the first deliverable step would be for `specreduce` to accept `Array` outputs from `ccdproc`.

- In addition to the high priority objectives, another major objective will be working closely with the newly NASA-funded EPRV community pipeline project. This is the next step up from the EPRV common data format project that I worked with and has been successfully completed. This work will include:
    - Attend the scheduled in-person meetings and monthly online tag-ups.
    - Work with EPRV pipeline teams to identify commonalities that could be better standardized and ported upstream into `specreduce` and/or `specutils`.
    - Work with community pipeline team on integrating `specreduce` and `specutils` into their work.

- Participate in spectroscopy and astropy dev calls and tag-up

### Approximate Budget
Currency: USD $

- Salary:
    - $9600 (full proposal based on 80 hours at current contracted rate of $120/hour)
    - $4800 (minimum SpectrumDM proposal based on 40 hours at current contracted rate of $120/hour)

Please note that we would happily accept budget items other than the above.

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
