# Reviewing affiliated packages

This document describes the set of review criteria for packages applying to
become Astropy-affiliated, and is intended for reviewers.

If you are reading this because you have accepted to review an affiliated
package submission, thank you for taking the time to do this!

<b>Your review and identity will be public.</b>

Reviewing a package involves assessing how well the package does in several
areas, which we outline below. As a reviewer it is is expected that you review
on these criteria, and it is sufficient to *solely* use these criteria .
However, feel free to bring up any other aspect which you think is important.

The basic reviews follow pyOpenSci standards:

* [Reviewer Guide](https://www.pyopensci.org/software-peer-review/how-to/reviewer-guide.html) is for you.
* [Editor Guide](https://www.pyopensci.org/software-peer-review/how-to/editors-guide.html) is for the Astropy Editor working with you.

In addition to the above, here are some Astropy-specific guidelines:

```markdown
#### Astropy-specific

- [ ] **Relevance to astronomy/astrophysics:**
    - [ ] **Out of scope:** Not useful for astronomers, or specific to one project/collaboration. (This is a basis for rejection.)
    - [ ] **Specialized package:** Useful to astronomers working in a very specific domain/field, or with a specific telescope instrument and usable not just by a single collaboration but any astronomers within that domain. Packages such as sncosmo fall into this category.
    - [ ] **General package:** Package that is useful for astronomers across more than a single field/instrument/telescope. Packages such as astroquery or astroplan fall into this category.
- [ ] *Integration with Astropy ecosystem:*
    - [ ] **No integration:** Does not use Astropy or other Astropy Affiliated packages anywhere where it should be possible, and/or uses other libraries instead, or unnecessarily duplicates functionality found in Astropy or other Astropy Affiliated packages. (This is a basis for rejection.)
    - [ ] **Partial integration:** Makes an effort to use Astropy or other Astropy Affiliated packages in places, but still has other places where this could be done.
    - [ ] *Good integration:* Uses Astropy or other Astropy Affiliated packages wherever possible. Where not, there are good reasons not to.
```

For specific actionable items, reviewer or editor are free to open issues on the package repository
directly and link them back to the application (this would be a GitHub issue in [pyOpenSci software submission repository](https://github.com/pyOpenSci/software-submission/issues). If some of the issues are to justify a rejection, that must be made clear in the review.

When in doubt, please consult with Astropy Affiliated Package Editors.
