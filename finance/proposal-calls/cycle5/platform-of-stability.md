### Astropy as a platform of stability in the astronomy software landscape

### Project Team
This proposal is to support Clément Robert's continued software engineering work
on the astropy core library and ecosystem.

### Project Description / Scope of Work

Astropy lies at a unique and critical position in the Python software stack
supporting astronomy and astrophysics; it is both the core library to a vibrant,
but domain specific ecosystem, and dependent on hundreds of other packages. As
such, astropy is required to provide a stable platform for a wide range of
(constrained) use cases, and should be as resilient as possible to upgrades.
Furthermore, since existing APIs are used accross vastly diverse contextes, their
evolution, when deemed necessary, must be handled with care and stretch over
long time spans.

This FR supports the on-going effort to improve the stability of astropy on 3
different time scales:

- (immediate term) handling day-to-day compatibility issues throughout the ecosystem
- (medium term) tackling long standing issues through planned API evolutions
- (long term) eliminating avoidable failure modes in CI

It short, this is aimed to reduce friction for both users and developers.

Hereafter is a (non-exhaustive) breakdown of more specific issues in the scope of this
proposal

- providing a high quality bedrock of backward compatibility
- coordinating with upstream and downstream stake holders to improve testing on a range
  of deployment environments
- improve portability and re-usability of binary artifacts (fundamental work was
  already conducted, and tracked in
  https://github.com/astropy/astropy/issues/18163, but more can be done in the
  near future)
- simplify the development process for most contributors to the core library (reduced build times)
- improve testability and test coverage of low level extension modules
- improve long-term maintainability of new APIs through developer documentation
  and code reviews
- tackle long standing bugs
- fix incompatibilities with development versions of core and secondary dependencies as needed
- extend support to future features of the Python interpreter (like JIT compilation and free-threading)
  - https://github.com/astropy/astropy/issues/16916
- handle long-term API evolutions through deprecation cycles
- solidify deprecation cycle guidelines and utilities
  - https://github.com/astropy/astropy/issues/18852
  - https://github.com/astropy/astropy/issues/18951

#### Roadmap Items

The proposed work aligns with the following roadmap items:

- Improve and/or maintain interoperability with performant I/O file formats and libraries such as HDF5 and Dask.
- Improve support for using Astropy tools in heterogeneous computing environments such as cloud environments or GPU systems.
- Support JIT compilation (e.g., numba, JAX, etc.) throughout Astropy core and coordinated packages.
- Increase the learning and mentoring opportunities for people interested in becoming contributors and helping to develop existing contributors into maintainers.


#### Project / Work / Deliverables

Minimal (non-exhaustive) and concrete deliverables are listed hereafter:

- reproducible builds in "oldestdeps" testing environments (https://github.com/astropy/astropy/issues/18782) 
- split out extension modules to a `astropy-core` package (https://github.com/neutrinoceros/astropy-APEs/pull/1)
- ensure compatibility with PEP 803/809 (the future of CPython's Limited API for 2026)
  throughout coordinated packages
- reforge astropy's configuration discovery system to improve maintainability and
  unblock missing features https://github.com/astropy/astropy/issues/18964
- developer guidelines for maintainable new APIs (email)
- detailed, quarterly reports of bug reports closed and PRs reviewed

### Approximate Budget
Currency: US
Budget: $50,000 to $80,000

I'm requesting funding for 500 to 800 hours of contractual work, over a performance
period of one year, and at a rate of 100$/hr.
I estimate 500 hours as a minimal viable budget to reach a majority of the goals
previously laid out, but more can be done with a larger budget.

### Period of Performance

2026 (Jan 1 to Dec 31)
