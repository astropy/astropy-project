# The Astropy Roadmap
**Latest revision: April 2022**

- [Introduction](#Introduction)
- [Status Legend](#Status-Legend)
- [Project Board](#Roadmap-2021-Project-Board)
- [Functionality](#Functionality)
- [Hardware and Performance](#Hardware-and-Performance)
- [Learn and User Support](#Learn-and-User-Support)
- [Community Building and Sustainability](#Community-Building-and-Sustainability)
- [Infrastructure, Documentation](#Infrastructure-Documentation)
- [Government, Management, and Personnel](#government-management-and-personnel)

## Introduction

This Roadmap captures high level actionable items that we as a project aim to undertake to improve the health and stability of the Astropy project. The Roadmap itself is a static document, while specific issues and efforts can be linked through [meta issues](#Roadmap-Meta-Issues). The Roadmap document will be revisited regularly at the Astropy coordination meetings, to keep track of progress and write new versions as needed.

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
  
## Roadmap Meta Issues

Meta issues in this repository associated with Roadmap items can be found [here](https://github.com/astropy/astropy-project/issues?q=is%3Aopen+is%3Aissue+label%3ARoadmap). Work done anywhere in the project that is relevant to the Roadmap can be tied to the appropriate meta issue for visibility.

## Functionality

- :large_orange_diamond: Provide next-generation spectroscopic reduction, analysis, and visualization tools usable by individual researchers and larger surveys.

- :large_orange_diamond: Improve support and validation for input/output of standard file formats used in Astronomy including FITS and HDF5 as well as compression handling and enhanced support for large tables.

- :large_orange_diamond: Improve interoperability and compatibility, while reducing duplication, amongst Astropy-affiliated packages and other community standard software.

## Hardware and Performance

- :large_orange_diamond: Improve Astropy ecosystem stability in High-Performance Computing environments, and expand options for compatibility with read-only filesystems.

- :red_square: Improve and/or maintain interoperability with performant I/O file formats and libraries such as HDF5 and Dask.

- :red_square: Improve support for using Astropy tools in high-performance machine learning and data analysis frameworks, such as on GPU systems.

## Learn and User Support 

- :green_circle: Improve discoverability of documentation and educational materials by overhauling the Learn website, including implementing an integrated search functionality and building an example gallery.

- :large_orange_diamond: Expand and build on workshop offerings by recruiting and training more facilitators and expanding the geographic diversity of meetings where we offer workshops. 

- :green_circle: Expand the number and diversity of user support resources, including establishing a user-focused forum on Discourse.

- :large_orange_diamond: Generate and ingest guides and/or a series of tutorials that demonstrate Astropy Project functionality in the context of astronomical research, especially focusing on spectroscopy tasks.

- :red_square: Develop tutorials suitable for use in university astronomy courses. 

## Community Building and Sustainability

- :large_orange_diamond: Increase the learning and mentoring opportunities for people interested in becoming contributors and helping to develop existing contributors.

- :large_orange_diamond: Increase inclusion, diversity, and empowerment efforts within the Astropy Project and NumFOCUS communities, and improved our understanding the demographics of our communities in order to measure the effectiveness of these efforts.

- :large_orange_diamond: Better understand Astropy user community through a NumPy-like user survey (see [this summary](https://numpy.org/user-survey-2020-details/) of their results).

## Infrastructure, Documentation

- :large_orange_diamond: Improve documentation for infrastructure setup, as well as the developer documentation.

- :red_square: Implement robust performance benchmark reporting for pull requests.

- :red_square: Implement integration testing for core, coordinated, and infrastructure packages.

## Government, Management, and Personnel

- :large_orange_diamond: Develop a process for recruiting, selecting, and managing personnel to complete Project priorities that require external personnel.

- :red_square: Define and document the process for categorization of core, coordinated, and affiliated packages.

- :red_square: Improve the process for recruiting and onboarding maintainers, paying particular attention to packages that are lacking maintainers.
