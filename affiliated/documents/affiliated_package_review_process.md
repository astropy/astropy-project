## Procedure for the proposal, review, and acceptance of Astropy-affiliated packages

This document describes the procedure for proposing, reviewing, and making a
decision about Astropy-affiliated packages. This is meant as a record of the
procedure and not the first place people should go to for - for instructions
on proposing an affiliated package, see **Becoming an Affiliated Package** on
[this](http://www.astropy.org/affiliated/index.html) page.

### Proposing an affiliated package

*These are written as if to the affiliated package author*

Once you believe your package is ready to submit for review by the
Astropy project, you should open a pull request to the
[astropy.github.com](https://github.com/astropy/astropy.github.com)
repository, modifying the ``affiliated/registry.json`` file to add details
about your own package. If you are not comfortable with git, you can do this
easily by accessing [this
link](https://github.com/astropy/astropy.github.com/edit/master/affiliated/registry.json)
which takes you directly to an editor. If you get a message saying **You need
to fork this repository to propose changes** then click on the green button
to confirm the forking:

<p align="center">
  <img src="images/propose_fork.png" alt="fork" width="600">
</p>

Copy the following template entry and fill out the
details:

    {
      "name": "Your package name",
      "maintainer": "Your name <your email address>",
      "stable": true,
      "home_url": "URL to the home page or documentation",
      "repo_url": "URL to the repository",
      "pypi_name": "PyPI name if it exists, set to an empty string otherwise",
      "description": "A few sentence description of your package",
      "review": {
         "functionality": "To be filled out by the reviewer",
         "ecointegration": "To be filled out by the reviewer",
         "documentation": "To be filled out by the reviewer",
         "testing": "To be filled out by the reviewer",
         "devstatus": "To be filled out by the reviewer",
         "python3": "To be filled out by the reviewer",
         "last-updated": "To be filled out by the reviewer"
     }
   },

then add it at the top of the ``registry.json`` file, starting on line 3,
after:

    {
      "packages": [

Once this is done, under **Propose file change** you can enter a short
description for the commit then click on the green **Propose file change**
button:

<p align="center">
  <img src="images/propose_commit.png" alt="commit" width="650">
</p>

On the next screen, check the changes you made, and click on the green
**Create pull request** button:

<p align="center">
  <img src="images/propose_create_1.png" alt="create_1" width="600">
</p>

Finally, give a title to the pull request such as **Proposed affiliated
package: your package name** and include a short description of the
package, then click on **Create pull request**:

<p align="center">
  <img src="images/propose_create_2.png" alt="create_2" width="600">
</p>

Once this is done, send an email to https://groups.google.com/forum/#!forum/astropy-dev
(which is the main developer list) to introduce your package and say that
you would like it to be considered as an affiliated package. Make sure you
include a link to the pull request you opened above.
