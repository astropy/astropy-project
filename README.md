# Astropy Project-wide repository

Documents and policies regarding the Astropy Project as a whole.  *Drafts* of policies under consideration go into the `drafts` directory.  Other directories can be created as needed to maintain organization, but as a general guideline a new directory should not be created unless it contains (or will contain) at least 3 files.

Additionally, the issue tracker will be used to discuss larger Project-wide issues. (I.e., those that are not particular to a specific pacakge or other repository.)

## If you locally cloned this repo before 15 June 2021

The primary branch for this repo has been transitioned from ``master`` to ``main``.  If you have a local clone of this repository and want to keep your local branch in sync with this repo, you'll need to do the following in your local clone from your terminal:
```
git fetch --all --prune
# you can stop here if you don't use your local "master"/"main" branch
git branch -m master main
git branch -u origin/main main
```
If you are using a GUI to manage your repos you'll have to find the equivalent commands as it's different for different programs. Alternatively, you can just delete your local clone and re-clone!
