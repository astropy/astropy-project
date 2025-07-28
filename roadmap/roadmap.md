# The Astropy Roadmap
**Latest revision: July 2025**

- [Introduction](#Introduction)
- [Status Legend](#Status-Legend)
- [Functionality](#Functionality)
- [Infrastructure, Documentation](#Infrastructure-Documentation)
- [Interoperability and compatibility](#Interoperability-and-compatibility)
- [Hardware and Performance](#Hardware-and-Performance)
- [Learn and User Support](#Learn-and-User-Support)
- [Community Building and Sustainability](#Community-Building-and-Sustainability)
- [Governance, Management, and Personnel](#government-management-and-personnel)


See the [Roadmap Completed Items](COMPLETED.md) page for items that have been completed and removed from the roadmap.

## Introduction

This Roadmap captures high level actionable items that we as a project aim to undertake to improve the health and stability of the Astropy project. The Roadmap itself is a static document, however it will be revisited regularly at the Astropy coordination meetings or via pull requests, to keep track of progress and write new versions as needed.

This Roadmap may also be used to prioritize the allocation of Project resources.

## Status Legend

### Green :green_circle:
- Group or person leading effort is identified and sufficiently supported.
- Effort is already underway and/or expected to be implemented in the “near term.”

### Orange :large_orange_diamond:
- Item is already defined (e.g., issue, APE exists), but not sufficiently underway.
- Attempts to secure the necessary resources are underway.
  - *For example, funding applied for, but not awarded.*

### Red :red_square:
- Consensus of the community is that the item is a priority.
- Attempts to secure the necessary resources have not yet been started.
  - *For example, there’s no one available to write a funding proposal or lead recruitment efforts.*


## Functionality

The core product of the Astropy Project is high quality astronomical software, including both the core library and Astropy Affiliated packages. This category encompasses goals having to do with this core Project functionality.

- :green_circle: Provide next-generation spectroscopic analysis tools usable by individual researchers and larger surveys.

- :green_circle: Add quantity support for non-NumPy arrays.

- :red_square: Determine a plan for long-term support of FITS, while also improving performance and making contribution easier.

- :large_orange_diamond: Improve support for reading and writing ASDF throughout the Astropy ecosystem (e.g., coordinated packages).

- :large_orange_diamond: Improve support for reading and writing spectra using the IVOA SpectrumDM.

- :red_square: Identify and ensure progress on longstanding issues that should be high priority (e.g., issues in io.votable).

## Infrastructure, Documentation

Underlying all Astropy packages is critical infrastructure that ensures high quality, well-documented software is released. This category encompasses goals having to do with such infrastructure and documentation.


- :large_orange_diamond: Maintain and improve robust performance benchmark reporting.

- :large_orange_diamond: Improve integration of core package and coordinated package documentation from a user perspective (e.g., joint search functionality).

## Interoperability and compatibility

One of the core principles of the Astropy Project is to "foster an ecosystem of interoperable astronomy packages." This category encompasses goals related to that principle of interoperability and compatibility.

- :green_circle: Improve support and validation for input/output (I/O) of standard and user-defined file formats used in astronomy by improving the unified I/O system.

- :large_orange_diamond: Improve interoperability between unit packages (e.g., `astropy.units`, `pint`, `unyt`).

- :large_orange_diamond: Encourage usage of the core and coordinated package ecosystem more directly (e.g., provide an `astropy-ecosystem` metapackage, or change `astropy` to `astropy-core` and make `astropy` the metapackage).


## Hardware and Performance

Astronomers perform their work in a variety of computing environments with a variety of requirements. This category encompasses goals related to supporting the performance and hardware needs of Astropy Project users, as well as anticipating future needs and requirements.

- :large_orange_diamond: Improve and/or maintain interoperability with performant I/O file formats and libraries such as HDF5 and Dask.

- :red_square: Improve support for using Astropy tools in heterogeneous computing environments such as cloud environments or GPU systems.

- :red_square: Add basic PyScript/WebAssembly support in Astropy.

- :red_square: Support JIT compilation (e.g., numba, JAX, etc.) throughout Astropy core and coordinated packages.


## Learn and User Support

The Astropy Project cannot succeed in its core objectives without a robust user onboarding and support system. This category is for items related to the Astropy Learn ecosystem and other user support related improvements.

- :green_circle: Generate and ingest guides and/or a series of tutorials that demonstrate Astropy Project functionality in the context of astronomical research.

- :red_square: Update Astropy website to reflect the Project as a whole, not just the core package.

- :green_circle: Develop tutorials that demonstrate the use of Astropy for spectroscopy tasks.

- :red_square: Expand and build on workshop offerings, including online and increased geographic coverage.

- :large_orange_diamond: Develop, host, and index tutorials suitable for use in university astronomy courses.

## Community Building and Sustainability

As a community-driven project, the long term health and development of the Astropy community is an intrinsic part of the Project. This category encompasses goals related to growing and maintaining that community, and ensuring that it adheres to the core principles of inclusion and consensus-building.

- :green_circle: Better understand Astropy user community through user and developer surveys (e.g., [Astropy User Survey](https://docs.google.com/presentation/d/1D2L8PE3gbzaIvgmlTmhoSD5f0QLAln0HbCghZmdgmeQ/edit?usp=sharing) and Organization Mycology surveys on [Astropy Community Engagement](https://astropy-report.orgmycology.com) and [Community views on diversity, equity, and inclusion in the Astropy project](https://astropy-dei.orgmycology.com)).

- :red_square: Increase the learning and mentoring opportunities for people interested in becoming contributors and helping to develop existing contributors into maintainers.

- :red_square: Increase inclusion, diversity, and empowerment efforts within the Astropy Project and NumFOCUS communities, and improve our understanding of the demographics of our communities in order to measure the effectiveness of these efforts.

- :red_square: Ensure people who contribute are from a broad experience base, including typical astronomers.

## Governance, Management, and Personnel

This category encompasses goals related to governing and managing the Astropy Project to facilitate reaching the goals described elsewhere in this document.

- :green_circle: Adopt the NumFOCUS Code of Conduct (CoC) and build a community ombuds/CoC team to curate the guidelines and enforce them.

- :red_square: Recruit for unfilled team positions.

- :green_circle: Define and staff the strategic planning role.
