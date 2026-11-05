### Migrating astropy's build system

**Proposal Category**: Innovations

### Project Team
Clément Robert (@neutrinoceros)

### Project Description / Scope of Work
I propose replacing the historical build tool chain
(`setuptools`/`setuptools-scm`/`extension-helpers`) with `meson-python`, which
is in line with migration already conducted in highly regarded packages in our
ecosystem such as `numpy`, `scipy` or `matplotlib` to name a few.

There are a couple important benefits to such a migration, such as:
- enabling incremental rebuilds
- truly editable installs for compilled components
- improved stability (setuptools is legacy software that's very hard ·to advance
  or improve)
- faster adoption of modern packaging standards (e.g. PEP 803)
- staying close to the stakes of our own core dependencies

I already implemented similar migrations in other packages I maintain, such as
- [`gpgi`](https://github.com/neutrinoceros/gpgi/pull/269)
- [`ewah-bool-utils`](https://github.com/yt-project/ewah_bool_utils/pull/187)
- [`h5py`](https://github.com/h5py/h5py/pull/2886) (in PR)
- [`bottleneck`](https://github.com/pydata/bottleneck/pull/511) (in PR)

If time and funding allows, I would handle this migration for all coordinated
packages with compiled/low level modules. With a restricted budget, I could
still advocate for it and consult with stakeholders to help them implement the
migration.

#### High Priority Objectives

- O3
- O5
- O6

#### Project / Work / Deliverables
Dropping setuptools as a build-time dependency for astropy is the only
deliverable. I favor switching to meson-python specifically because I already
have experience with it and there's a significant precedent for it within our
immediate ecosystem, but an alternative exists (`scikit-build-core`) which much
of the same benefits. This proposal would remain relevant if the community
expressed a different preference.

### Approximate Budget
Currency: US $

- Salary / contractor fees : $4,400
  I request 40hr at a rate of $110/hr
- TOTAL : $4,400

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
