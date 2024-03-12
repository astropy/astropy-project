### Title

Research Software Engineer: User and Developer Support

### Project Team

- Clément Robert (@neutrinoceros)
- Moritz Guenther (@hamogu)

### Project Description

In the last cycle, we had two open hires for an 
[RSE position](https://github.com/astropy/astropy-project/blob/main/finance/proposal-calls/cycle3/user-dev-support-rse.md). One of them (Clément) is available to continue this work in 2024 and this
proposal is to continue funding for him at a similar level as before for the next 12 months.


### Project / Work

We ask to fund a research software engineer (RSE) position to
tackle both user-facing and developer-facing support issues, as identified and
prioritized by the Astropy community and infrastructure teams. The RSE (Clément) is expected to
work independently, but with feedback from Astropy community and a dedicated contact
(Moritz).
We envision about an equivalent ~50% FTE appointment, but that can be scaled
based on the available budget.

We propose to essentially continue to work done by the RSE's in cycle 3. 
See [invoices for the RSE work from the last cycle](https://github.com/astropy/astropy-project/issues/360)
for a list of work done so far.

There are three themes to that:

#### 1 - Long standing bugs and issues

Astropy has > 1200 open issues, some of them more than a decade old. This is a combination of bugs, feature requests, and ideas, and not all of them are directly actionable. However, hundreds of them *are* bugs and feature requests, often untouched by volunteer contributors for years.

While astropy clearly thrives with those bugs and issues, each of them represents at least one user
who was stopped in their work and found this annoying enough to open an issue. We know anecdotally, that
many users who do not think of themselves as "developers" don't open issues on github (e.g. they might not 
even have an account) so each bug probably represents several or more users who have run
into a problem. For a smooth user experience, we should close out bugs and fill in feature requests
where we can.

The RSE shall tackle a number of long-standing issues and
bugs as listed in the issue trackers for the core package and the coordinated packages;
more bugs and issues are available than can be addressed by this position, so the
choice of which ones to address will be guided by community input.

#### 2- Support current fires

Astropy has few required dependencies, but changes in new versions of pytest, numpy-dev, or sphinx can make
CI on all new PRs fail. In coordination with Pay Lian and others, Clément
did significant work to keep astropy up-to-date with numy-dev in the transition to numpy 2.0 so far. While that
is mostly done, he will support changes in pytest or future numpy version as they come up. How much work
this is and when it's required is hard to predict, but having Clément available with a significant number
of hours per week to fix these things as they come up eases the development process for all
other contributors, in particular occasional volunteer developers who might not be used to diagnose
CI failures that have nothing to do with their own changes.

#### 3 - Astropy Roadmap

The RSE shall work on the items listed on [Astropy Roadmap]
(https://github.com/astropy/astropy-project/blob/main/roadmap/roadmap.md), that the
community has already prioritized, but not yet found the resources to implement. The current roadmap
is almost a year old and most of the items that would be appropriate for this position are under
development by the current RSE hires or other astropy contributors, even though they are still marked
as orange or red in the roadmap. However, the roadmap will be updated in the next Astropy coordination 
meeting, which will take place just a few weeks after Clement would start on this contract.
We expect that he will pick up one or two items from the new roadmap.




### Approximate Budget

Budget breakdown (nominal):

- Contractor fees: $98000 (approx. $90/hour for 20 h/ week for 12 months)

### Period of Performance
1 year