### Specreduce Development and Project Management

### Project Team

- Hannu Parviainen


### Project Description / Scope of Work

This proposal requests funding to support my continued development and project 
management work on Specreduce.

The main goal of the proposed work is to ensure that Specreduce provides a 
complete, reliable, and user-friendly toolset for the reduction of long-slit 
spectra, supported by comprehensive and approachable documentation, examples, 
and tutorials. Once this stage is complete, the next phase will extend 
Specreduce’s capabilities to support multi-object spectrographs.


#### Roadmap Items

- :large_orange_diamond: *"Improve integration of core package and coordinated 
  package documentation from a user perspective."*
  
    - A major component of this proposal involves improving the clarity and 
      structure of the Specreduce documentation.  Ongoing work can be followed in 
      [Specreduce PR #275](https://specreduce--275.org.readthedocs.build/en/275/).
    
- :large_orange_diamond: *"Develop, host, and index tutorials suitable for use 
  in university astronomy courses."*
  
  - The documentation work will include the creation of fully worked tutorials 
  and teaching materials, such as the [LHIRES-III tutorial](https://github.com/hpparvi/specreduce_example_lhires/blob/main/example_1.ipynb)  that can be directly used in teaching spectroscopy in a university setting.
  
- :red_square: *"Support JIT compilation (e.g., numba, JAX, etc.) throughout 
   Astropy core and coordinated packages."*
   
  - The newly developed functionality will be accelerated using Numba where 
    appropriate, and existing routines can also be optimized (without changing 
    the API) once all user-visible features are in place. (I have used Numba 
    extensively in my own packages since 2016 and consider myself fairly
    familiar with it.)


#### Project / Work / Deliverables

- Complete the development of missing or partially implemented specreduce core 
  functionality, including:
  - flux calibration,
  - uncertainty propagation, and
  - PSF-based spectral extraction.

- Implement the infrastructure required for multi-object spectrograph data 
  reduction.

- Create a fully defined set of tutorials and educational materials for 
  spectroscopic data reduction using Specreduce. These materials will be 
  published as a “Learn Astropy” guide and will include step-by-step *recipes* 
  covering common spectroscopic reduction tasks for a variety of instruments 
  and setups.

- Continue Specreduce project management and maintenance, including:
  - reviewing pull requests and managing GitHub issues,
  - coordinating community contributions,
  - preparing and publishing new releases,
  - maintaining synchronization between PyPI and Conda distributions, and
  - ensuring alignment with Astropy’s development and contribution guidelines.

  
### Approximate Budget

The proposed budget is based on an hourly rate of USD 150 and an anticipated 
workload of 1–4 hours per week over nine months, from April to December 2026 
(the first three months are funded by an existing project). This corresponds 
to a total of 36–144 hours, resulting in an estimated project cost of 
USD 5,400–21,600.

### Period of Performance

April 1, 2026 – December 31, 2026
