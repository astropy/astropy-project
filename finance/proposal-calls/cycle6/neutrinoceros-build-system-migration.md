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

This proposal collides with https://github.com/astropy/astropy-project/pull/557,
by the same author, but isn't incompatible with it. Both proposed changed can be
implement over the same cycle, just not at the exact same time. If bot proposals
were accepted and funded, the order of operations would be left as an adjustment
variable, especially considering that this one is a solo project but "astropy as
pure Python project" is a team effort.


#### High Priority Objectives
None

#### Project / Work / Deliverables

The project will start with the production of an APE to define the exact
migration path, goals and non goal. If consensus is reached and the APE is accepted, the rest of the budget will be dedicated to implementation. Otherwise,
any remaining budget will be left untouched.

Dropping setuptools as a build-time dependency for astropy is the only
deliverable. I favor switching to meson-python specifically because I already
have experience with it and there's a significant precedent for it within our
immediate ecosystem, but an alternative exists (`scikit-build-core`) which much
of the same benefits. This proposal would remain relevant if the community
expressed a different preference.

### Approximate Budget
Currency: US $

- Salary / contractor fees : $4,950 I request 45hr at a rate of $110/hr, the
  first 5 of which will be dedicated to writing the APE
- TOTAL : $4,950
  minimal useful budget: $550 (just the APE)

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
