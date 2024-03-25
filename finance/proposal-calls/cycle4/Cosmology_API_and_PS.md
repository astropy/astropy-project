### Title
Support for updating the API of Cosmology and implementing a Power Spectrum module.

### Project Team

- This is an open hire for a software engineer. 
- Supervised by [Nathaniel Starkman](https://github.com/nstarman)
- Consulting with [Nicolas Tessore](https://www.ucl.ac.uk/astrophysics/people/dr-nicolas-tessore)

### Project Description

Myself and Nicolas Tesssore wrote an API, called [`The Cosmology API`](https://cosmology.readthedocs.io/projects/api/en/latest/) with the intent to adopt it in Astropy to improve the `astropy.cosmology` interface and set the stage for future improvements like supporting more Array libraries as function inputs and interoperability with other cosmology codes.

I think we should hire someone to implement the The Cosmology API in `astopy.cosmology`, which will require some deprecation and backwards compatibility code as well as (almost entirely backwards compatible) changes of the Cosmology interface and test suite.

In addition, a major missing component of the API is a proposal for a power spectrum module. This job would be to review the major cosmology codes to understand their structure and to draft a power spectrum module API (w/out the implementation). As a simple concrete step the hire would adapt an existing implementation (order 200 lines in [`SkyPy`](https://github.com/skypyproject/skypy/blob/module/power_spectrum/skypy/power_spectrum/_eisenstein_hu.py)) of a simple growth function for Astropy. The API  will serve as the template for the Astropy cosmology power spectrum module.

In sum:

1. Fully adopt the Cosmology API in `astropy.cosmology`
2. Review Cosmology code (`CAMB`, `CLASS`, `JAX_COSMO`) beyond the background to understand the overall structure of these codes.


### Project / Work

#### Cosmology API

Last year Nicolas Tessore and I collaborated to put in a lot of thought work about the API of `astropy.cosmology`, with the intent to establish an updated API that can:
1. be more consistent, in terms of attribute and method names and treatment of quantities
2. Build in methods to evaluate distance measures between redshifts.
3. Make it easier to create new cosmology classes, implementing only the required functionality.
4. Make it easy to statically type functions that require cosmology objects and to specify only the attributes and methods actually required by the function.
5. Make it easier for Astropy Cosmology to work with other Array libraries.

There are numerous benefits to the Cosmology API, unfortunately I have not had the requisite time to see the API implemented in Astropy.

I propose to hire a software engineer to complete the job of implementing the Cosmology API in Astropy. This will require (but is not limited to):
1. writing a C decorator to convert positional-or-keyword to positional-only arguments so as to enable backwards compatibility during the transition without introducing new function call overhead.
2. Adding methods in the API to Astropy, especially changing the distance measure functions from their current 1-argument form to allow for the optional second argument
3. Separating out the component classes from FLRW, as done in the API. This will enable new Cosmology classes like the pedagogically important radiation-only, matter-only, lambda-only cosmologies, as well as 2-component cosmologies.
4. Changing Omega_X to be unitless Quantites, not plain arrays
6. Updating the test suite to mach these changes in the code.
7. Updating the docs to match these changes.


#### Power Spectrum

A Power Spectrum module in Astropy has been an open Issue for a decade. Such a feature is foundational to a comprehensive cosmology module, yet it is absent in Astropy. While there are numerous specialized libraries dedicated to power spectra, the objective for Astropy is not to outperform these tools but to provide a solid foundational layer. The rationale is twofold: firstly, many users require only the basic functions provided by power spectra, which are often sufficient for a broad range of applications. Secondly, with the development of the Cosmology API, there's an opportunity to offer a seamless transition between Astropy and more specialized libraries. By establishing a basic power spectrum module, Astropy could serve as a starting point for cosmological calculations, allowing users to prototype their work before changing to more complex physics with dedicated tools. This approach not only enhances the utility of Astropy but also supports a more integrated and efficient workflow within the cosmological research community.

The primary objective for the software engineer in this project is to conduct a thorough review of the major cosmological codes currently in use, with the aim of developing an understanding of their structure. This foundational knowledge will then be applied to draft an initial version of a power spectrum module API, tailored specifically for integration within Astropy. There is prior art: [`Skypy` ](https://github.com/skypyproject/skypy/tree/module/power_spectrum/skypy/power_spectrum) has done a fair amount of work related to a clean implementation of a simple power spectrum and a simple growth function and has code we can (modify) and upstream to Astropy. What is lacking is a formal review of popular community codes to justify the API. 
The software engineer will carry out this review and then adapt the `SkyPy` code to the new API. As a note, the implementaiton does not require formal cosmological knowledge nor is the SkyPy code long, at a few hundred lines of code. The API class, once developed, is intended to serve as the cornerstone for the entire Astropy cosmology power spectrum module, setting a standard for future enhancements and iterations of the Cosmology API. This initiative is not only about extending the capabilities of Astropy but also about establishing a robust template that will guide the development of subsequent versions of the Cosmology API, ensuring that they meet the evolving needs of the astrophysical community.

#### Summary

The two projects of implementing the Cosmology API and developing a Power Spectrum API for Astropy are go hand-in-hand and are both important for a larger effort to make Astropy Cosmology a possible starting point for research-level cosmological analysis. Using a standardised Cosmology API, users will be able to template and set up a simplified analysis pipeline using Astropy. This initial prototyping phase is often a significant part of the research problems, which could be carried out using Astropy Cosmology alone. Once projects have sufficiently matured, use of a standardised API will allow researchers to easily move on to more complex tools at research level. By providing simple implementations of e.g. the growth function and an analytical power spectrum with a well-designed API, Astropy can start to be used in this crucial role.


### Approximate Budget

I estimate this project will take fewer than 200 hours. At 100 USD/hour, the budget is:

USD$ 20,000


### Period of Performance

This should take only six months.
