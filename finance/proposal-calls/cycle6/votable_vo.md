### Title
Improvements of astropy VO interoperability with a focus on improving VOTable

### Project Team
This is a proposal endorsed by the `io.votable` and `pyvo` maintainers to cover VO/VOTable relevant tasks that are identified as important for quite some time but require focused and dedicated development effort that is beyond their maintainer role.

Some of the maintainers (@andamian, @bsipocz, @tomdonaldson) are unable to contact this work but will coordinate on the identification of suitable domain expert individual(s). 
This proposal has been introduced at the IVOA interop meeting in November 2025, and we would like to explore avenues to contract with FR with CDS, especially with PyVO maintainer @ManonMarchand.


### Project Description / Scope of Work
Identify and ensure progress on longstanding issues with `io.votable`.

#### Roadmap Items

Directly addressing issues for VO(Table), priorities are to be determined by the `io.votable` and `pyvo` maintainers:

🟥 Identify and ensure progress on longstanding issues that should be high priority (e.g., issues in io.votable).

As well as addressing VOTable/VO related issues that arise from other development work; for example while addressing roadmap ite

🔶 Improve support for reading and writing spectra using the IVOA SpectrumDM.

The round tripping experience with VOTable is not exactly great; and this work should improve upon that topic, too, ultimately improving the interoperability for

🟢 Improve support and validation for input/output (I/O) of standard and user-defined file formats used in astronomy by improving the unified I/O system.

With the new contractor we also envision this project to contribute to these two cmmunity building roadmap items:

🟥 Increase the learning and mentoring opportunities for people interested in becoming contributors and helping to develop existing contributors into maintainers.

🟥 Ensure people who contribute are from a broad experience base, including typical astronomers.


#### Project / Work / Deliverables

- Identifying a new contractor for io.votable work.
- Triage and start addressing existing `io.votable` and `samp` issues.

List of open issues:

astropy.io.votable - https://github.com/astropy/astropy/issues?q=sort%3Aupdated-desc+is%3Aissue+is%3Aopen+label%3Aio.votable+
astropy.samp - https://github.com/astropy/astropy/issues?q=sort%3Aupdated-desc%20is%3Aissue%20is%3Aopen%20label%3Asamp, especially https://github.com/astropy/astropy/issues/9763

The actual issue triaging is attached to the PR description. 
We would start with the prioritization of fixing the bugs that are in the "one to n weeks of work" section (estimating around 2 to 3 months of work -- plus review cycle), and then chose a bundle of feature requests that would help achieving better VOTable integration in astropy's systems.

### Approximate Budget
Exact scope would be kept flexible and will be specified after the contractor is identified depending on their availability. Rate will be kept aligned with the other astropy contracts (and details may depends on if it's a sole contractor or subcontract to an Institute to "buy out" developer time).

For budgeting purposes we use the Aperio numbers for the estimated 2-3 months of full time effort: 40 x 8 x 150 -- 40 x 12 x 150 = $48000 -- $72000

### Period of Performance

Due to the expected delay with identifying the contractor we expect this project to start at the second half of the year; period of performance is Jun 1, 2026–Dec 31, 2026 with possible extension to the next year.
