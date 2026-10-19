# Cycle 6 funding requests and ideas

# Changes relative to the previous cycle

The primary changes for Cycle 6 (relative to Cycle 5) are that:

* There are now two main categories of proposals: _Operations_ and _Innovations_. Proposals should indicate which category they fall under. These categories are described below in turn.
* The original Astropy Roadmap is being replaced by a smaller number of high priority objectives for 2027, and funding proposals should indicate, if appropriate, which objective(s) they aim to address.

As for Cycle 5, due to funding uncertainties, the period of performance and budgets should be just one year, as opposed to multiple years.

# Proposal categories

This section describes the two main proposal categories. Proposals should indicate which category they fall under at the top under **Proposal Category** (see [Cycle 6 template](template.md)).

## Operations

Proposals that request funding to carry out work which is part of the responsibilities of a project role are classified as _Operations_. This is work that is essential to the sustainability and functioning of the project, but is not work that will ever be 'done'. Examples include participating in one of the Astropy committees, maintaining a core sub-package or coordinated package, and maintaining testing and documentation infrastructure. A full list of roles and responsibilities can be found on the [Astropy team](https://www.astropy.org/team.html) page. These proposals do not need to be tied to specific high priority objectives.

## Innovations

Proposals that do not fall under the _Operations_ category are classified as _Innovations_. These are typically time-bound projects that produce specific deliverables. It does not need to be a completely new project and may have been started in previous cycles, but it is for a specific project rather than to carry out whatever duties fall under a role.

Each proposal should fall under a single category. If you are planning work that includes both _Operations_ and _Innovations_ components, please submit these as separate proposals.

# High priority objectives

The Strategic Planning and Organizing Committee (SPOC) is currently in the process of organizing objectives and key results for a set of high priority objectives, and will be sending out information about this soon. In the meantime, to help you plan, the eight high priority objectives that have been selected for 2027 based on voting by the Astropy community are:

* Make astropy.units.Quantity a modern part of the Python array ecosystem by supporting any array-API-compliant backend, not just NumPy

* Identify ways in which we can ensure the wellbeing of our community in the age of LLMs

* Identify single points of failure throughout the infrastructure of the Astropy ecosystem

* Create a process to identify and ensure progress on longstanding issues that should be high priority

* Improve the sustainability and maintenance of coordinated and affiliated packages (this is specifically for projects that propose to do things to *improve* the sustainability and maintenance, rather than regular _Operations_ work)

* Identify the barriers to making Astropy work easily in cloud contexts

* Improve and maintain interoperability with performant I/O file formats and libraries

* Provide support for reading and writing spectra using the IVOA SpectrumDM in specutils

_Innovations_ proposals that go towards addressing one or more high priority objectives will be given a higher weight during funding allocations.

# Funding amount

We anticipate that for this funding cycle a maximum of **$330,000** (US) will be available for effort, split as follows:
* **$132,000** (US) for Operations proposals
* **$198,000** (US) for Innovations proposals

In addition, a maximum of **$82,000** (US) will be available for travel. Any travel costs should be listed as a separate line item in the proposal budget.

# Period of Performance

The period of performance should be for one year. Ideally, Jan 1–Dec 31, 2027.

# What can the funding be used for?

Money can be used for travel, subscriptions, etc., in addition to direct financial support to individuals, including individuals based outside of the United States.

Funding requests may be submitted even if they include the recruitment and hiring of another person to complete the task. See below: Open Hire Process.

The funds currently come from a NASA ROSES grant. NumFocus, the Project’s fiscal sponsor, and the Finance Committee assume responsibility for ensuring that all budgets are consistent with any applicable funding agency rules.

# Funding Request Process Overview

As for Cycle 5, we envision a two stage FR process to enable the community to discuss and improve ideas, to merge teams with similar ideas, and for the SPOC to ensure as many of the high priority objectives as possible are being addressed.

* Nov 6, 2026: **_Draft_** FR Deadline
* Two week iteration and discussion period during which draft FRs can be fleshed out and modified. During this time:
  * The SPOC may submit and/or solicit new proposals that fill gaps not addressed by the initial round of requests.
  * The Finance Committee will review budgets and may provide feedback and/or request more information.
* Nov 20, 2026: Finalized FRs are due, two week Voting period begins
* Dec 7, 2026: The SPOC and Finance Committee will work together to select funding requests and allocate budgets.
* Dec 18, 2026: Announcement of selected FRs. Drafting contracts begins.
* Jan 1, 2027: Work can commence once contracts are signed.

Note that these dates are nominal, and unplanned events like extended government shutdowns could extend some of the dates/deadlines.

FRs shall foster the Astropy Project goals of community, shared work, and cooperation and shall be described, reviewed, and executed in this manner.

We aim to achieve broad consensus before the vote. Requesters are encouraged to combine ideas and teams, modify, or withdraw FRs during the discussion period, as appropriate. Discussion is open to anyone; it is not restricted to voting members.

Voting members of the Astropy Project vote on the FRs using thumbs up/down on a dedicated comment. Every voting member of the Astropy Project has equal voting rights.

The SPOC and Finance Committee will select FRs based on the voting results, alignment with the high priority objectives (for _Innovations_ proposals), confirmation of available people to implement, and available funds.

# How to Submit a Funding Request
Funding Requests (FRs) should be posted as pull requests to https://github.com/astropy/astropy-project/ with the initial title text "Cycle 6 Funding:". The goal is to make this process as easy as possible for everyone, so we impose a limit of 100 lines assuming 80 char/line. We provide a template: [Cycle 6 template](template.md). Please place the file with your FR in the [Cycle 6 folder](.), the same location as the template.

# Post-request process

Once selection is completed, an FR that is *not* selected does not continue further, although it can always be re-proposed. It is also possible that if more funds become available before the next cycle, a proposal may be accepted later but with a revised timeline.

If an FR *is* selected, 🎉! Now the work begins.

Once a proposal is accepted, the Finance Committee will assign a committee member contact to ensure invoices are submitted, process is followed, etc. At the same time, the Coordination Committee will assign a COTR (see below) for that FR.

The following general steps follow when an FR is selected:

1. The FR is assigned a final budget and funding source, and the PR is merged.
2. A new tracking issue is created for the FR (by the finance committee member contact), which includes the budget, period of performance, and identifies the assigned COTR.
3. Work updates are given in the tracking issue, although out-of-band clarifications/conversations with the finance committee contact or COTR are welcome. It is the responsibility of the COTR to ensure these updates happen (although they don't necessarily need to be done by the COTR themselves).
4. As work is completed, the funded personnel or their institutional representative submit invoices to NumFocus.
5. The issue is closed when the FR's work is completed, the budget is exhausted, or the period of performance expires.

# COTRs

As in the last two cycles, all proposals will be assigned a COTR (Contracting Officer's Technical Representative). This concept is borrowed from government funding agencies, although it is to be stressed that Astropy's goal is to make the COTR role as low-overhead as possible.

The COTR's key responsibilities include:

* Technical expertise: COTRs are experts in the contract's specific area, evaluating the contractor's performance with their technical knowledge.
* Contract compliance: COTRs monitor and ensure the contractor follows contract terms, reviewing deliverables to meet expected Astropy community standards.
* Performance evaluation: COTRs assess contractor performance, verifying the work meets contract expectations.
* Issue resolution: COTRs play a role in resolving issues or disputes, collaborating with the finance committee, the Coordination Committee, and the broader Astropy Project.
* Communication and reporting: Acting as a liaison, COTRs ensure transparent communication and report progress and issues (see above).


# Fostering constructive discussion

We want to stay true to the "radical transparency" ethos of the Project and thus we are asking the community to comment on the FRs publicly. At the same time, we want to ensure that the conversations stay as constructive as possible to foster the Astropy Project’s commitment to maintaining a positive and welcoming culture. Thus, here we provide some example language that might help commenters stay constructive with their comments.

Examples of non-constructive comments are:

* “This is not worth our time.”
* “Person X has never really done anything that I think is good.”

Examples of constructive comments are:

* “This is probably not a good way to spend Project funds because package abc already provides the same functionality.”
* “It's not clear to me the value that this would bring to the Project. Do the proposers have a way of assessing impact?"
* “I’m concerned the project team does not have the necessary skills to get this done. Can the team offer more proof of expertise, or bring in help from team members who have more relevant expertise?"

If you are worried about your comments being perceived as inappropriate, you are welcome to send your feedback directly to the Finance Committee at finance@astropy.org or ask on Slack. You are also welcome to use the “thumbs down” vote without adding comments. If you have any concerns about this process and the ensuing discussion that you would prefer to discuss privately, contact the ombudsperson at confidential@astropy.org.

# Open hire process

FRs can include an “open hire” process to identify people to undertake the activities described. Should such a request be accepted, the Finance Committee will organize a recruitment process to find the right person (or people) to carry out the work. Members of the FR team will be asked to assist in the recruitment and hiring process. The number of open hire requests selected may be limited by Finance Committee staffing availability.

We envision a recruitment process that expands beyond the US Astronomy community and would include the various Research Software Engineering forums in addition to the AAS Job Register. We are in the process of putting together a hiring guide.

# Template and examples

The following is a template proposal: [template.md](template.md). You can also refer to successful **Finalized** FRs from previous cycles:

* [Cycle 2](https://github.com/astropy/astropy-project/tree/main/finance/proposal-calls/2021-proposal)
* [Cycle 3](https://github.com/astropy/astropy-project/tree/main/finance/proposal-calls/cycle3)
* [Cycle 4](https://github.com/astropy/astropy-project/tree/main/finance/proposal-calls/cycle4)
* [Cycle 5](https://github.com/astropy/astropy-project/tree/main/finance/proposal-calls/cycle5)
