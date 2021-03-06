# Call for Astropy ideas / projects to be funded in 2021

## Goals
Projects and ideas funded through this process shall improve The Astropy Project. This includes code for the core repository, for coordinated or affiliated packages, infrastructure (e.g. testing, CI), tutorials, workshops, notebooks, community engagement, inclusion, diversity and empowerment, travel to conferences or meetings, talks, mentoring, and anything else broadly Project related. This does not have to be a new initiative, but can be ongoing work (e.g. maintain the CI), but cannot include work that is already otherwise paid for (e.g. if you have a NASA grant to maintain the CI, you cannot bill for the same work twice).

Suggested projects shall foster the Astropy Project goals of an open and inclusive community, shared work, and cooperation and shall be proposed and executed in this manner.

Total funding for this call is coming from the Moore grant and 200,000 $ are available in total in the period spring 2021 to spring 2022.

Project suggetions need to clearly identify what the funding is used for (e.g. "pay YYY $ to add Klingon Standard Time to astropy.time" or "organize astropy workshop to engage amateur astronomer community in Antarctica")

*Note: You can think of this as an internal "proposal process" to allow the community to select exactly where the money that the Astropy Project has will be spend. To avoid confusion with the external proposal that gave the money to Astropy (here: Moore foundation), we use the term "suggested project" and "project team" here.*

## Details

- Source of money: Moore grant
- Specific area: Most of the money can be distributed to any area deemed important by the community. However, we do have specific budgets for work related to spectroscopy (22500 US $), mentoring contributors (15000 US $), and first contributor workshops (12000 US $).
- Restrictions: This is a world-wide call, open to all past, current, and future contributors to the Astropy project. (Because the funding is held in a US bank account and administered by a US-based institution, the proposed work cannot be done in a United States embargoed country or otherwise be prohibited by US sanctions or export controls, see https://home.treasury.gov/policy-issues/financial-sanctions/sanctions-programs-and-country-information for a list).

## Process
### Suggestion
Project ideas should be posted as pull requests to github.com/astropy/astropy-project/ with the initial title text "Funding 2021:".
Please open the PR to add a file in the following directory: finance/proposal-calls/2021-proposal/
The goal is to make this process as easy as possible on everyone, so we impose a limit of 100 lines assuming 80 char/line. We provide a template below.
We envision a two stage process to enable the community to comment and improve ideas, teams with similar ideas can merge to avoid duplicated work, etc..

- Discussion can start as soon as PRs are posted
- April 5th, 12:00 UTC: Draft Deadline (after this date, no new projects)
- Two week dedicated discussion and idea modification period
- 2021-04-17: Deadline for finalized text
- Finance Committee reviews project ideas for compatibility with grant conditions
- 2021-04-24 to 2021-05-08: Discussion and voting

*Rationale: We aim to achieve community consensus before the vote. Proposers may combine ideas and teams or withdraw suggested projects during the discussion period.*

On 2021-04-17, the text for the projects is frozen but comments are still allowed. Within 7 days of this deadline, the Finance Committee will review all projects to ensure they are compatible with the terms of the currently available funding sources and should be included in the list to be voted on.

### Discussion
We want to stay true to the "radical transparency" ethos of the Project and thus we are asking the community to comment on these funding requests publicly. At the same time, we want to ensure that the conversations stay as constructive as possible to foster the Astropy Project’s commitment to maintaining a positive and welcoming culture. Thus, here we provide some example language that might help commenters stay constructive with their comments:

Example of non-constructive comments are

- “This is not worth our time.”
- “Person X has never really done anything that I think is good.”

Examples of constructive comments are

- “This is probably not a good way to spend Project funds since package abc already exists which provides the same functionality.”
- “It's not clear to me the value that this would bring to the Project. Do the proposers have a way of assessing impact?"
- “I’m concerned the project team does not have the necessary skills to get this done. Can the team offer more proof of expertise, or bring in help from team members who have more relevant expertise?"

If you are worried about your comments being construed as non-constructive, you are welcome to send your feedback directly to the Finance Committee at finance@astropy.org or ask on Slack. You are also welcome to use the “thumbs down” vote without adding comments.  If you have any concerns about this process and the ensuing discussion that you would prefer to discuss privately, contact the ombudsperson at confidential@astropy.org.

### Voting and decision
Voting is done by adding a "thumbs up" to a dedicated comment that will be added to the project PR discussion once the voting period has opened. Any number of projects can be voted up by a single person. The Interim Finance Committee reserves the right to discount votes from GitHub accounts without any contributions to Astropy repositories.

The CoCo and the Finance Committee will select projects following the community up/down votes and taking into account the requirements of the available grant funding (e.g. if none of the highest ranking projects deals with spectroscopy, the money reserved for spectroscopy can be awarded to the highest ranking spectroscopy project, even if that means that other, higher ranked projects won't be executed).

*Rationale: This is similar to how e.g. ESO or HST proposals as awarded. Technically, the TACs suggest a list of proposals for the director, who is free to pick in any way they like. However, the TAC ranking is followed unless there are strong reasons against it (e.g. a scheduling requirement cannot be accommodated). This process is well accepted in the astro community and thus it makes sense to follow it here.*

## Who will be paid to do work?
Money can be used for travel, infrastructure, equipment etc, but in many cases, money will be used to pay people to do work for Astropy. In that case, the following approaches can be used:

- Projects can list one or more people who will perform the work and any needed budget to support the work.
- The project team can alternatively not commit to the work themselves, but promise to organize a job search, accept applications, and select a candidate within 6 months of the project being accepted. Contact details of the selected person are then forwarded to the Interim Finance Committee. The project team is not paid for work time associated with the search.

In either case, the Interim Finance Committee will take care of the formal process of setting up statements of work, signing contracts, and reviewing invoices. Other funding strategies that we have not anticipated will also be considered.

Note: The Interim Finance Committee realizes that this process may lead to a number of parallel, possibly competing searches by different groups of people. We expect all searches to follow the code of conduct with respect to fairness, non-discimination etc. Any violation should be brought the Interim Finance Committee or the Astropy Ombudspersion (confidential@astropy.org). If these procedures are violated, funding for that specific project will not be granted. Projects planning to do a search should include the cost of job listings in their budget.


## Template for project suggestion
```
### Title

### Project team

### Project Summary
How does this benefit Astropy packages / users/ community / ...? Short summary.

### Project / work
Details here as needed for Astropy community members to understand what is planned.

### Budget
currency: US $

Include overheads, fringe etc. if money is paid as sub-grant (note that the Moore grant caps overhead at 15%).

- Travel:
- Conference Registrations:
- Salary / contractor fees etc. (give sum here, details about contract, payment method (contract/sub-award) etc. can be worked out with the finance committee later)
- TOTAL
```
