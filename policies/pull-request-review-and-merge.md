# Astropy Project Pull Request Review & Merging Policy

## Astropy Core Package

When submitting a pull request (PR) in the Astropy core package the following
process must take place before it can be accepted. If the pull request fails any
of the reviews or checks it must be amended and undergo additional review before
being accepted.

### Review & Approval

All pull requests will be reviewed by at least one contributor with relevant
expertise to ensure that:

  - New or updated code is correct and achieves the desired effect of
    either fixing a bug or making an enhancement.
  - New tests or modifications to tests are adequate to cover the code changes.
    Tests for edge cases exist where applicable and judged to be sufficiently
    important.
  - There are no API changes or the API changes are well-understood and
    acceptable and beneficial on the whole to the Astropy user community, and
    are documented as an API change in the changelog.
  - Formatting and style maintain the existing style of a package and
    readability of the code base for future developers.

Reviews will be detailed and should include review and suggestions at the
line-by-line level, although "I looked and had no comments" is a valid answer

For pull requests that require specific knowledge of a sub-package, a maintainer
of the sub-package that the contribution affects is required to approve. For
other less complex cases, for example a documentation improvement, review may be
conducted by any Astropy core package maintainer.

While a core package maintainer does not have to be the one performing the
review, if the review is performed by someone else, that maintainer is
responsible for ensuring the contributor review is sufficiently detailed and
follows these guidelines.

After successful review, the maintainer(s) will formally approve the pull
request.

While we welcome pull requests for anyone, pull requests that are purely related
to code formatting or restructuring without change in functionality (including,
but not limited to, the use of automated tools) may in some cases be closed
without review, since these kinds of changes can cause unecessary conflicts with
other pull requests, or may not line up with the coding style or wishes of the
current maintainer(s). In these cases, it should be made clear to the contributor
that we still value their interest in contributing to the project, but point
them to this policy to explain that we cannot always accept these kinds of
changes.

### Additional Checks

Additional checks will be performed to verify that there are no other issues
with the pull request, for example:

- A release manager or maintainer will check that the selected release milestone
  is suitable for the scope of the change.  In particular bug-fix backports are
  considered where feasible and sensible. Documentation is usually backported.
  API changes or new feature changes are not backported unless under special
  circumstances.
- A matrix of CI checks will be run to ensure that all existing tests pass on
  supported platforms. Even CI jobs that are allowed to fail should still pass
  unless a known and unrelated failure occurs; i.e., look at the logs even in
  the event of a green check mark.
- An automated tool will check that the change log mentions the change and PR
  number and that the change log section used matches the selected release
  milestone set by the maintainer.

### Merging

The pull request will be merged once it is approved by relevant maintainers (as
described above) and has passed all necessary checks. This can be done by any
core package maintainer. In practice this is sometimes the PR developer and
sometimes the reviewer.

## Astropy Coordinated & Infrastructure Packages

The process of PR approval for coordinated and infrastructure packages should be
the same as the process for the core package except that reviews and approvals
can be done by any maintainer. Coordinated and infrastructure packages should
have at least two maintainers with push access and all PRs should be approved by
at least one of the other maintainers. Any maintainer can then merge the pull
request once it is approved.

## Astropy Affiliated Packages

The change process for affiliated packages is largely at the discretion of the
package maintainers. Affiliated packages may make their requirements as rigorous
or as lenient as they like. However, the Astropy Project does require that
affiliated packages maintain the code under version control on a publicly
available site.

In most cases packages are hosted on GitHub or GitLab and updated via pull
requests, but this is not a requirement. Independent review is encouraged but is
at the discretion of the package maintainer(s) as some packages may be largely
developed by a single maintainer. Please see the affiliated package’s
documentation for more information.
