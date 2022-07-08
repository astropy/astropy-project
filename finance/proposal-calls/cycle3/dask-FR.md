### Title
Make `Quantity` and `nddata` compatible with Dask

### Project Team
This is an open hire, to be overseen by Erik Tollerud (@eteq), although he welcomes others who want to drive this idea more.

### Project Description
The [Dask](https://www.dask.org) project has dramatically expanded the compute capabilities of the Python numerical ecosystem by providing a way to scale it naturally beyond "numpy-sized" workflows. However, the core Astropy data structures `nddata` and `units.Quantity` do not really support Dask (see e.g. (#8227)[https://github.com/astropy/astropy/issues/8227] and several other issues linked from there).  This project is an open hire to find someone willing to solve this problem. 

### Approximate Budget
Roughly 16000 USD, based on a *very* rough estimate of 160 hr (i.e., ~ 1 full month) at $120/hr