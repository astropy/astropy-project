# Cycle 4 funding requests and ideas


# Changes relative to the previous cycle

The primary changes for this Cycle relative to Cycle 3 are a single funding source (NASA), and the addition of the COTR role (see below).

TBD ...
* COTR wording needs proofreading
* Dates need updating
* Budget amount


# Funding goals

Funding requests (FR) shall improve the Astropy Project. This includes work on code for the core repository, for coordinated or affiliated packages, infrastructure (e.g. testing, CI), tutorials, workshops, notebooks, community engagement, inclusion, diversity and empowerment, and anything else broadly Project related.

FRs shall foster the Astropy Project goals of community, shared work, and cooperation and shall be described, reviewed, and executed in this manner.

FRs need to clearly identify how the the funding will be used (e.g. "pay $YYY (US) to add Klingon Standard Time to astropy.time" or "organize astropy workshop to engage amateur astronomer community in Antarctica")


# Funding amount

We anticipate a maximum of **TBD** (US) to be available for this funding cycle.  We urge the community to **aim high**, either by ambitious and/or expensive proposals for their own work, or by bringing in new members via the “open hire” process (outlined below).

# Period of Performance

Each FR should specify how long the project will last (the "Period of Performance"). A project can be anywhere from 1-3 years. For ongoing projects longer periods of performance are better, as that lowers the administrative overhead of the project. In particular, FRs for subawards are best done with longer periods of performance e.g. 3 years.

Note that if your proposal has a longer Period of Performance than one year, funds beyond that horizon are contingent on funds from the project being available.


# What can the funding be used for?

Money can be used for travel, subscriptions, etc, in addition to direct financial support to  individuals.

The funds currently come from a NASA ROSES grant. It includes the following general areas:

* Basic maintenance and development on all aspects of the Project 
* Project-wide infrastructure
* Affiliated packages
* Astropy Learn and Community Engagement

The Finance Committee assumes responsibility for ensuring that all awards made are consistent with any applicable funding agency rules.


# Funding Request process

Funding Requests (FRs) should be posted as pull requests to https://github.com/astropy/astropy-project/ with the initial title text "Cycle 4 Funding:". The goal is to make this process as easy as possible for everyone, so we impose a limit of 100 lines assuming 80 char/line. We provide a template below. Please place the file with your FR at https://github.com/astropy/astropy-project/tree/main/finance/proposal-calls/cycle4 (the same location as the template).

We envision a two stage FR process to enable the community to discuss and improve ideas, teams with similar ideas to merge, etc.

* March 1: **_Draft_** FR Deadline (new requests after this date will not be reviewed this cycle)
* Three week iteration and discussion period during which draft FRs can be fleshed out and modified
* March 22: Finalized FRs are due
* Finance Committee reviews for compatibility with legal conditions
* March 29 - April 5: voting period

We aim to achieve broad consensus before the vote. Requesters are encouraged to combine ideas and teams, modify, or withdraw FRs during the discussion period as appropriate.

At the second deadline, the text for the FRs is frozen but comments are still welcome. Discussion is open to anyone; it is not restricted to voting members. Within 7 business days of this deadline, the Finance Committee will review all requests to ensure they are compatible with the terms of the currently available funding sources and should be included in the FRs to be voted on.

After that, voting members of the Astropy Project (as of the start of the vote) vote on the FRs using thumbs up/down on a dedicated comment.  Every voting member of the Astropy Project has equal voting rights.

The Coordination and Finance Committees will select FRs following the ranking by the members, taking into account the discussion, available effort level to implement, and any restrictions associated with the available funds.

# Post-request process

Once selection is completed, an FR that is *not* selected does not continue further, although it can always be re-proposed.  It is also possible that if more funds become available before the next cycle, a proposal may be accepted later but with a revised timieline.

If an FR *is* selected, 🎉! Now the work begins. 

Once a proposal is accepted, the finance committee will assign a committee member contact to ensure invoices are submitted, process is followed, etc.  At the same time, the Coordination Committee will assign a COTR (see below) for that FR.

The following general steps follow whan an FR is selected:

1. The FR is assigned a final budget and funding source, and the PR is merged.
2. A new tracking issue is created for the FR (by the finance committee member contact), which includes the budget, PoP, and identifies the assigned COTR.
3. Work updates are given in the tracking issue, although out-of-band clarifications/conversations with the finance committee contact or COTR are welcome. It is the responsibility of the COTR to ensure these updates happen (although they don't necessarily need to be done by the COTR themselves).
4. As work is completed, the funded personnel or their institutional representative submit invoices via OpenCollective (exact details of this will be clarified for each issue as details vary from person-to-institution).
5. The issue is closed when the FR's work is completed, the budget is exhausted, or the period of performance expires.

Note that if your proposal has a longer Period of Performance than one year, funds beyond that horizon are contingent on funds from the project being available.

# COTRs

New this Cycle, all proposals will be assigned a COTR (Contracting Officer's Technical Representative).  This concept is borrowed from government funding agencies, although it is to be stressed that Astropy's goal is to make the COTR role as low-overhead as possible.

COTR's key responsibilities include:

* Technical expertise: COTRs are experts in the contract's specific area, evaluating the contractor's performance with their technical knowledge.
* Contract compliance: COTRs monitor and ensure the contractor follows contract terms, reviewing deliverables to meet expected Astropy community standards.
* Performance evaluation: COTRs assess contractor performance, verifying the work meets contract expectations.
* Issue resolution: COTRs play a role in resolving issues or disputes, collaborating with the finance committee, the Coordination Committee, and the broader Astropy Project.
* Communication and reporting: Acting as a liaison, COTRs ensure transparent communication, and reporting progress and issues (see above).


# Fostering constructive discussion

We want to stay true to the "radical transparency" ethos of the Project and thus we are asking the community to comment on these funding requests publicly. At the same time, we want to ensure that the conversations stay as constructive as possible to foster the Astropy Project’s commitment to maintaining a positive and welcoming culture. Thus, here we provide some example language that might help commenters stay constructive with their comments.

Example of non-constructive comments are:

* “This is not worth our time.”
* “Person X has never really done anything that I think is good.”

Examples of constructive comments are:



* “This is probably not a good way to spend Project funds because package abc already provides the same functionality.”
* “It's not clear to me the value that this would bring to the Project. Do the proposers have a way of assessing impact?"
* “I’m concerned the project team does not have the necessary skills to get this done. Can the team offer more proof of expertise, or bring in help from team members who have more relevant expertise?"

If you are worried about your comments being perceived as inappropriate, you are welcome to send your feedback directly to the Finance Committee at finance@astropy.org or ask on Slack. You are also welcome to use the “thumbs down” vote without adding comments. If you have any concerns about this process and the ensuing discussion that you would prefer to discuss privately, contact the ombudsperson at confidential@astropy.org.


# Open hire process

FRs can include an “open hire” process to identify people to undertake the activities described. Should such a request be accepted, the Finance Committee will organize a recruitment process to find the right person (or people) to carry out the work. Members of the FR team will be asked to assist in the recruitment and hiring process. The number of open hire requests selected may be limited by Finance Committee staffing availability.

We envision a recruitment process that expands beyond the US Astronomy community and would include the various Research Software Engineering forums in addition to the AAS Job Register. To further help with recruitment, we may partner with a consulting firm with expertise in the open source scientific python ecosystem. The exact details and scope of this depend on how many proposals in this Cycle are open hire requests.


# Template and examples

The following is a template proposal: [template.md](template.md). We also include an [example](example_draft_FR.md) that is an acceptable **Draft** FR (due July 8) to emphasize that drafts can include minimal information and are meant to be fleshed out and modified based on feedback before the final deadline (Aug 19). You can also refer to successful Cycle II **Finalized** FRs at [this link](https://github.com/astropy/astropy-project/tree/main/finance/proposal-calls/2021-proposal).
