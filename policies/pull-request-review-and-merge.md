# Policy on pull request review and merging in the Astropy Project

## Astropy core

In the astropy core package the requirements are as follows:

- At least one contributor with relevant expertise must review the pull request
  in detail.
  - New or updated code is logically correct and achieves the desired effect of
    either fixing a bug or making an enhancement.
  - New tests or modifications to tests are adequate to cover the code changes.
    Tests for edge cases exist, if applicable.
  - There are no API changes or the API changes are well-understood and
    acceptable and beneficial on the whole to the astropy user community.
  - The expected level of review is detailed, including review and suggestions
    at the line-by-line level.  Formatting and style are acceptable points for
    comment, in particular to maintain the existing coding style of a package and to
    maintain readability of the code base for future developers.
  - Maintainer(s) of subpackages that the contribution affects are required to
    approve the pull request for changes that require specific knowledge of a
    subpackage.  Other less complex cases, for example a documentation
    improvement, may be reviewed by any astropy core package maintainer.
  - While a maintainer does not have to be the one doing the detailed review, if
    the detailed review is by someone else, the maintainer is responsible for
    ensuring the contributor review is sufficiently detailed and follows these
    guidelines.
  - Following a successful review, maintainers should formally approve the pull
    request.
- A release manager or maintainer checks that the selected release
  milestone is suitable for the scope of the change.  In particular bug-fix
  backports are considered where feasible and sensible.
  Documentation is usually backported. API change or new feature changes
  are not backported unless under special circumstances.
- A matrix of CI checks ensure that all existing tests pass on supported
  platforms. Even the CI job that is allowed to fail should pass unless
  an known and unrelated failure occurs; i.e., look at the logs even in
  the event of green check mark.
- A bot checks that the change log mentions the change and PR number and that the change log
  section used matches the selected release milestone set by the maintainer.
- Merging the pull request can be done by any core package maintainer once
  approved by relevant maintainers (as described above).  In practice this is
  sometimes the PR developer and sometimes the reviewer.

## Astropy coordinated and infrastructure packages

The process should in general be similar to the core package, although since a
number of coordinated and infrastructure packages have fewer maintainers, the
concept of subpackages is not relevant. Nevertheless, all coordinated and
infrastructure packages should have at least two maintainers with push access.
All changes to these packages should be done via pull requests, and approved by
at least one of the other maintainers (any maintainer can then merge the pull
request provided it is approved).

## Astropy affiliated packages

The change process required by the Astropy Project for affiliated packages are
substantially less rigid than in the Astropy core package. However, each
affiliated package may make their requirements as rigorous as they’d like.
- It is required to maintain the code under version control on a publicly
  available site.
- In most cases packages are hosted on GitHub or GitLab and updated via pull
  requests, but this is not a requirement.
- Independent review is encouraged but is at the discretion of the package
  maintainer(s).  In particular some packages may be largely developed by a
  single maintainer.
