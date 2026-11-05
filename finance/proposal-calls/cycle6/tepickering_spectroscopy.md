### Spectroscopy Development

**Proposal Category**: Innovations

### Project Team
Timothy Pickering

### Project Description / Scope of Work
This a continuation of spectroscopy development and outreach carried out in previous cycles as well tackling two spectroscopy-related high-priority objectives.

#### High Priority Objectives
- Add read/write support for the IVOA SpectrumDM format to `specutils`.
- Begin the work of supporting the `Array` interface protocol in `specreduce`. This ties into both the work being done to make `Quanitity` `Array` compliant as well as improving interoperability with performant I/O file formats and libraries that `Array` would facilitate.

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

- Salary: $9600 (based on 80 hours at current contracted rate of $120/hour)

Please note that we would happily accept budget items other than the above.

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
