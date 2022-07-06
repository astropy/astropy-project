### Title

### Project Team

Nathaniel Starkman (NS) and Dan Foreman-Mackey (DFM)


### Project Description

[`Quantity`][Quantity] is a backbone of Astropy, leveraging the power of [NumPy]
[NumPy] and adding units. However, the computing landscape is changing. Many
numpy-like libraries exist for different use cases: [Dask][Dask] for
distributed computing, [CuPy][CuPy] for GPU, [xarray][xarray] for labeled
data, [JAX][JAX] for autograd and GPU acceleration, [zarr][zarr] for compressed
arrays, etc. Though these libraries offer a numpy-like API and interoperability
protocols, `Quantity` is incompatible with them, which prevents users from
choosing the most suitable library while also having units. In other words,
users working on larger-than memory data or doing machine learning, among other
use cases, struggle to use Astropy.

Therefore, we propose to determine how best to extend `Quantity` to support
numpy-like libraries and all the use cases they confer. This entails creating a
plugin architecture and a reference implementation, starting with JAX
(crucial for machine learning).


### Project / Work

There are two components to this project:

1. Extension to the Quantity framework to allow [`Quantity`][Quantity] to be
abstracted from subclassing [`numpy.ndarray`][NumPy] and to instead use a
broader range of base classes. NS is currently developing this approach in
https://github.com/astropy/astropy/pull/12921. This framework will support the
use of, for example, a JAX array as the storage back end for a `Quantity` when
appropriate. This will be a plugin architecture with 3rd party library support
housed in a to-be-proposed affiliate (preferably coordinated) package.

2. Connect JAX with the new Quantity framework. There are two options to make
this work:
    - Issue / PR to JAX to support custom tracer objects, which are conceptually
      similar to function overrides offered by NumPy. DFM is already discussing
      this with some members of the JAX development team.

    - If (a) is not possible, wrap JAX’s numpy. DFM already has a package `jpu`
      with a reference implementation that will serve as the basis of this
      work.


### Deliverables

Given how deeply numpy is embedded in Quantity, e.g. the use of in-memory
``.view()``, extending Quantity to other libraries will introduce changes.
Therefore, our work will be to:

1. Create a reference implementation for both the Astropy changes and the
affiliate package, detailed in the previous section.

2. Write a report of our findings.

These two results will serve either as the basis for a future PR / APE, if the
approach succeeds; or as an explanation why the options explored are not
suitable for Astropy, along with recommendations for other approaches.


### Future Work

This project is to determine a path forward for Astropy to support the next
generation of array libraries. With a reference implementation and detailed
report the community will be able to provide input on next steps. We suggest
the following as possible future works:

1. An Astropy Proposal for Enhancement to complete and roll out the reference
implementation. This would presumably include the affiliate/coordinated package
for 3rd party library integrations.

2. An Astropy Proposal for Enhancement for the alternative implementation
suggested in the report.

3. A grant proposal (e.g. for phase 4) to fund this future work and ensure a
smooth transition and long-term support for the current Quantity framework.


### Approximate Budget

For NS:
Target budget: $8,400 for 70 hours of work at $120/hour (rate negotiable).

For DFM:
Dan Foreman-Mackey is graciously donating his time and expertise.


[Quantity]: https://docs.astropy.org/en/stable/units/quantity.html
[NumPy]: https://numpy.org/doc/stable/reference/generated/numpy.ndarray.html
[Dask]: https://www.dask.org
[CuPy]: https://cupy.dev
[xarray]: https://docs.xarray.dev/en/stable/index.html
[JAX]: https://jax.readthedocs.io/en/latest/notebooks/quickstart.html
[zarr]: https://zarr.readthedocs.io/en/stable/
