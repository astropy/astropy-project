# Homeier: Functionality and I/O of multiple spectra in Astropy and Specutils

**Proposal Category**: Innovations

### Project Team
Derek Homeier

### Project Description / Scope of Work

- Work on infrastructure for multi-Spectrum objects

#### High Priority Objectives
None, though performance tests for new loaders would contribute to [O7](https://astropy-roadmap.readthedocs.io/en/latest/#o7-improve-and-maintain-interoperability-with-performant-i-o-file-formats-and-libraries);
however no Key Result is expected to be completed just by this work.

#### Project / Work / Deliverables

- Support redshift/radial velocity arrays in SpectrumCollection
  ([astropy/specutils#1319](https://github.com/astropy/specutils/issues/1319) 
   by designing a `radial_velocity` model for SpectralCoord supporting arrays
   orthogonal to the spectral axis ([astropy/astropy#19560](https://github.com/astropy/astropy/issues/19560);
   [astropy/astropy#19576](https://github.com/astropy/astropy/pull/19576))

- Write round-tripping writers/loaders for SpectrumList and potentially SpectrumCollection

- Participate in Spectroscopy Dev telecons (12 hrs total).

### Approximate Budget
Currency: US $

- Salary under independent external contractor agreement: 4 hours weekly for 45 weeks,
  a total of 180 hours (accounting for holidays) @ $120 / hour

- TOTAL: $21,600

- Minimum viable amount: any part of the above work package at $5,400 for 1 hr / week,
  which would go with priority into extending the `SpectralCoord` model in `astropy.coordinates`.

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
