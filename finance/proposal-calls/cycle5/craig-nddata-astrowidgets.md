### Array API and Astrowidgets

### Project Team
The project team will be Matt Craig.

### Project Description / Scope of Work
This is a continuation of the ROSES 2020 project "Array API and astrowidgets."
The goal of this project is to i) make `ccdproc` and `astropy.nddata` compatible
with the [Array API standard](https://data-apis.org/array-api/latest/) and ii)
improve and expand the `astrowidgets` package for interactive visualization of
astronomical images.

#### Roadmap Items
This project addresses these this roadmap item:

+ "🟥 Improve support for using Astropy tools in heterogeneous computing
  environments such as cloud environments or GPU systems."
    + One of the array libraries that will be supported as part of the Array API
      is CuPy, which enables use of NVIDIA GPUs for array computations.
    + Astrowidgets and the Astronomy Image Display API (AIDA) are intended to
      support development of browser-based interactive image display tools that
      can be used in cloud computing environments.

#### Project / Work / Deliverables
Please see the [issue tracking the original
proposal](https://github.com/astropy/astropy-project/issues/411) for details of
the work proposed. `ccdproc` and `astropy.nddata` will be made Array
API-compliant to the extent possible without modifying code in  `Quantity` or
other parts of the Astropy core that are not directly under the scope of this
proposal. A object-oriented interface for image combination will be added to
`ccdproc`. THe `ginga` and `bqplot` backends that implement
[AIDA](https://aida.readthedocs.io/) will be finalized and better documented.
Additional backends (e.g. `plotly`) may be added if time allows.

### Approximate Budget
Currency: US $9,487.50

- Contractor salary: $9,487.50
- TOTAL: $9,487.50

Please see discussion of the budget details in the discussion on the [issue for
the Cycle 4
proposal](https://github.com/astropy/astropy-project/issues/411#issuecomment-3207064721).

### Period of Performance

The period of performance is Jan 1, 2026–Dec 31, 2026.
