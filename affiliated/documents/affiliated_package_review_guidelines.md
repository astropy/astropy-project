# Reviewing affiliated packages

This document describes the set of review criteria for packages applying to
become Astropy affiliated.

Note that we use the following color-coding, which also determines if a package is accepted after its first review:

<table>
<tr>
<td width=100><img src="https://img.shields.io/badge/Red-red.svg" alt="Red"></td>
<td>Affiliated packages can only be accepted into the list if there are no red scores. Existing affiliated packages that have one category that drops down to red don’t get automatically kicked out, but they should resolve this, otherwise the package will be de-listed.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Orange-orange.svg" alt="Orange"></td>
<td>Having orange scores is fine, but is both a warning to the user that not all is perfect about the package, and an incentive for developers to improve and reach green.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Green-brightgreen.svg" alt="Green"></td>
<td>This is the standard we want all packages to aim for. Packages that have all-green scores may be featured in a separate table for well-maintained and supported packages.</td>
</tr>
</table>

The document also includes ``monospaced keywords`` for the categories and levels.  These are the keywords and values to be used in the [registry.json](http://www.astropy.org/affiliated/registry.json) file that is the canonical source for affiliated package information.

The categories and levels are the following:

* Functionality (``'functionality'``)
* Integration with Astropy ecosystem  (``'ecointegration'``)
* Documentation (``'documentation'``)
* Testing (``'testing'``)
* Development status (``'devstatus'``)
* Python 3 compatibility (``'python3'``)

### Functionality ('functionality')

We first need to make sure that the scope of the package is relevant for the affiliated package system. The scopes are:

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Out%20of%20scope-red.svg" alt="Out of scope"></td>
<td>Not useful for astronomers, or specific to one project/collaboration.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Specialized%20package-brightgreen.svg" alt="Specialized package"></td>
<td>Useful to astronomers working in a very specific domain/field, or with a specific telescope instrument and usable not just by a single collaboration but any astronomers within that domain. Packages such as sncosmo fall into this category.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/General%20package-brightgreen.svg" alt="Green"></td>
<td>Package that is useful for astronomers across more than a single field/instrument/telescope. Packages such as astroquery or astroplan fall into this category.</td>
</tr>
</table>

Note that general is not necessary better than specific, it’s just a way to make sure we can present these separately.

### Integration with Astropy ecosystem  ('ecointegration')

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Red-red.svg" alt="Red"></td>
<td>Does not use Astropy or other affiliated packages anywhere where it should be possible, and/or uses other libraries instead.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Orange-orange.svg" alt="Orange"></td>
<td>Makes an effort to use Astropy or other affiliated packages in places, but still has other places where this could be done but isn’t</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Green-brightgreen.svg" alt="Green"></td>
<td>Uses Astropy or other affiliated packages wherever possible.</td>
</tr>
</table>

### Documentation ('documentation')

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Red-red.svg" alt="Red"></td>
<td>No documentation or some documentation, but very bare bones/minimal and incomplete or incorrect in a number of places.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Orange-orange.svg" alt="Orange"></td>
<td>Reasonable documentation (which could be a very well written README), installation instructions and at least one usage example, but some parts missing.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Green-brightgreen.svg" alt="Green"></td>
<td>Extensive documentation, including at least: motivation/scope of package, installation instructions, usage examples, API documentation. In terms of infrastructure, the documentation should be automatically built on readthedocs.org. If appropriate, one or more tutorials should be included in the Astropy tutorials at http://tutorials.astropy.org.</td>
</tr>
</table>

### Testing ('testing')

Note: In our terminology, “tests” refer to those that can be run in an automated way, and we do not consider examples that need to be run and/or checked manually to be acceptable as “tests”

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Red-red.svg" alt="Red"></td>
<td>No tests or tests that are not trivial to run or don’t use a standard testing framework, or low test coverage (no exact threshold for coverage since this is not always easy to measure, but in this category most of the code is not covered).</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Orange-orange.svg" alt="Orange"></td>
<td>A reasonable fraction of the code is covered by tests, but still some parts of the code that are missing tests. To be in this category, packages should use a standard framework (pytest, nose, etc.) and be runnable with a single command.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Green-brightgreen.svg" alt="Green"></td>
<td>Test coverage is very high (for example 90% or more), tests use a standard framework (pytest, nose, etc.) and are easy to run and continuous integration is used to ensure package stability over time.</td>
</tr>
</table>

Note that test coverage can be tricky to measure, so this will be carefully assessed for each package. We will not publish coverage percentages but rather indicate use the badges above to indicate whether it it low, medium or high compared to what one might realistically achieve.

### Development status ('devstatus')

<table>
<tr>
<td width=200><img src="https://img.shields.io/badge/Red-red.svg" alt="Red"></td>
<td>No active development/maintainers, even if stable releases exist, if package is not or no longer fully functional.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Heavy%20development-orange.svg" alt="Heavy Development"></td>
<td>Stable releases exist, but still under heavy development (so API changes can be frequent).</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Functional%20but%20unmaintained-orange.svg" alt="Functional but unmaintained"></td>
<td>Stable releases exist and there are no active developers/maintainers but package remains mostly functional.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Functional%20but%20low%20activity-orange.svg" alt="Functional but low activity"></td>
<td>Stable releases exist but the maintainers only make occasional comments/commits (and package is not in excellent condition, because otherwise it’s fine to have a completely stable package with little activity if it can be considered 'finished')</td>
</tr><tr>
<td><img src="https://img.shields.io/badge/Green-brightgreen.svg" alt="Green"></td>
<td>Package has stable releases, and package is actively developed (as needed). A metric for active development is whether most recently-opened issues have some kind of reply from maintainers.</td>
</tr>
</table>

### Python 3 compatibility ('python3')

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Red-red.svg" alt="Red"></td>
<td>Nothing is 'unacceptable' at this point, but once after 2020 ‘Only compatible with Python 2’ goes from orange to red.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Orange-orange.svg" alt="Orange"></td>
<td>Only compatible with Python 2</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Green-brightgreen.svg" alt="Green"></td>
<td>Compatible with Python 3</td>
</tr>
</table>
