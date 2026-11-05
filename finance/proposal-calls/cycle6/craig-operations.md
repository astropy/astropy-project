### ccdproc and astropy.nddata maintenance (Craig)

**Proposal Category**: Operations

### Project Team
The project team is Matt Craig.

### Project Description / Scope of Work
This proposal funds continued maintenance of the `ccdproc` coordinated package
and the `nddata` package in astropy core, extending the maintainer role from
Cycle 5 ([#515](https://github.com/astropy/astropy-project/issues/515)). Beyond
routine maintenance, I expect two larger items: keeping `NDData`/`CCDData` in
step with Array API adoption in the core, which supports the 2027 high-priority
objective of making `Quantity` work with any array-API-compliant backend, and
fixing longstanding performance problems in `ccdproc` image combination.

#### Project / Work / Deliverables
Deliverables:

- Respond to issues and pull requests in a timely manner.
- Move the Array API workarounds now in `ccdproc` into the core as it adopts the
  standard. Progress is tracked in
  [ccdproc#971](https://github.com/astropy/ccdproc/issues/971) and
  [astropy#15073](https://github.com/astropy/astropy/issues/15073). This should
  wait until the core is closer to Array API adoption, since several of the
  workarounds exist only because `Quantity` lacks Array API support.
- Make `ccdproc` image combination faster and leaner, addressing
  [ccdproc#645](https://github.com/astropy/ccdproc/issues/645),
  [ccdproc#624](https://github.com/astropy/ccdproc/issues/624),
  [ccdproc#1012](https://github.com/astropy/ccdproc/issues/1012) and
  [ccdproc#1013](https://github.com/astropy/ccdproc/issues/1013). In `reducer`
  I recently cut the time to combine 40 images of 4096×4096 pixels from 228 s
  to 4 s, with a very low memory limit, by reading
  each input once and combining in bands
  ([mwcraig/reducer#193](https://github.com/mwcraig/reducer/pull/193)); related
  changes roughly halved peak memory
  ([mwcraig/reducer#185](https://github.com/mwcraig/reducer/pull/185),
  [astro-notebooks#18](https://github.com/feder-observatory/astro-notebooks/pull/18)).
  Much of that work can move upstream into `ccdproc`.

### Approximate Budget
Currency: USD

- Salary: $4,000 (roughly 27 hours at the $150/hour rate of my current
  independent contractor agreement)
- Travel: $1,500 to sprint and recruit contributors at SciPy 2027. Sprints at
  SciPy 2026 produced several infrastructure contributions to `astrowidgets`
  from new contributors.
- TOTAL: $5,500

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
