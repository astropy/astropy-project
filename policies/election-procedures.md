# Astropy Election Procedures

## Overview

Astropy votes are managed with the [Helios Voting platform](https://heliosvoting.org) and
announced publicly via the astropy-dev mailing list and the OpenAstronomy Discourse forum. 

## Procedure for creating an election

1.  Set a date for the election and announce the election
    - This sets various deadlines that must be followed by nominees and voting members / CoCo nominees
    - Election start date must be at least 4 weeks after the announcement email
      - In announcement email, call for additional nominees
      - Deadline for nominations at least 2 weeks before election
      - The election is open for 2 weeks once it’s open
    - [See template email below](#Email-templates)
    - Send email to list of voting members (not just astropy-dev) - the email list in the
     Google drive. That way, you see if emails bounce and can hunt down a corrected email address
2. Collect nominees for new voting members / CoCo members and inform them
   - Collect nominations from roles survey and emails to coordination committee
   - Email nominees to inform them of nomination
   - Deadline to accept nomination 1 day before election opens
   - Inform nominees that to accept the nomination, they must send a few sentence description of
     their contributions to astropy and justification for voting member status to the CoCo 
     [See template email below](#Email-templates)
3. Post nominee statements to voting-members topic in OpenAstronomy Astropy Discourse
   - The election manager posts the nominee statements in the OpenAstronomy Discourse
      voting-members topic (private to only voting members, as described in APE0)
   - One post per nominee
4. Collect any additional ballot measures to be voted on (e.g., changes to APE0, etc...)
   - Post the ballot measures in the OpenAstronomy Discourse voting-members
   - One post per ballot measure
5. Set up the election on Helios Voting (see next section)

## Running an election with Helios

1. Log into [helios](https://vote.heliosvoting.org/)
2. Click “Create an election”
   - Short name convention: astropy-\<description\>-\<month\>-\<year\> 
     For example: astropy-voting-members-july-2022
   - Name convention: Astropy \<description\> — \<month\> \<year\> 
     For example: Astropy Voting Members — July 2022
   - Description: Write a one sentence description of the election
   - Check “Private?” to ensure that only registered voters can see the ballot
   - Voting starts at: select the predetermined date for the election to start
     (12:00 UTC for the time)
   - Voting ends at: two weeks after the start date
   - All other field left as default values
4. Now we have to add questions to the ballot. Click the “questions(0)” link to add a new question
   - Add one question for each nominee: “Do you support adding \<NAME\> as an Astropy voting member?”
     - Make each required by selecting “select between 1 and 1 answers”
     - Add “Yes”, “No”, “Abstain” as possible answers
   - Add one question for each ballot measure
     - Make each required by selecting “select between 1 and 1 answers”
     - Add “Yes”, “No”, “Abstain” as possible answers
5. Make sure the list of current voting members is complete
   - The list is in [google sheets](https://docs.google.com/spreadsheets/d/18VOl-EAwefcwi1aNLWXnZ0-a9WTBx4ry_QB8t23tYKw/edit#gid=0) (permission required).
   - Download the list as a CSV, remove the first row (the headers), and upload as registered voters
6. Freeze the ballot and set it to open voting at the start time
   - Go to the “voters & ballots” link and prepare / send an email with voting
     information to all voters
   - DO NOT copy paste to fill the “Body” section of the form, instead use that space to add
     any additional info you want to send to all voters.
7. After the ballot closes, “compute encrypted tally” and then “compute results”
   - Send the results email
8. Add newly voting members to organization
   - Create a PR to add any newly-added voting members to https://github.com/astropy/astropy.github.com
     (see https://github.com/astropy/astropy.github.com/pull/496 for an example)
   - Add new voting members and their emails to the google sheet


## Email templates

**Note:** any text in “\<\>” should be updated for future emails.

### Election announcement

Subject: Announcing Astropy Voting Member Election: \<July 2022\>

Dear Astropy Community,

The next Astropy Voting Member election will be on \<July 8, 2022.\>

We have already received some nominations from the Roles survey, but are accepting additional
nominations for new voting members until the end of \<June 21\> (anywhere on Earth).
To nominate someone (or yourself) to be a voting member, please fill out this form:
https://forms.gle/f1hi6MNEmw1RzYPY7 

For the Coordination Committee,
\<sender name\>

<hr/>

Subject: Announcing Astropy Coordination Committee Election: \<September 2022\>

Dear Astropy Community,

The next Astropy Coordination Committee (CoCo) election will begin on \<September 25, 2022\>.
One seat is available as \<name's>\ terms is coming to an end. The new member will serve a
3-year term. More details about the process are described in APE0.

Nominations are open now and will close on \<Friday, September 23\> (anywhere on Earth).
Anyone is welcome to nominate. To nominate someone (or yourself) to be a CoCo Member,
please fill out the Nomination Form: \<link\>.

Nominees will be asked via email whether they wish to accept their nomination.
If they accept, the nominee will be asked to provide a short statement on the
Open Astronomy Discourse.

For the Coordination Committee,
\<sender name\>

### Inform nominees

Subject: Accepting Nomination as an Astropy Voting Member

Dear \<NOMINEE\>,

Congratulations, you have been nominated to be a new voting member for the Astropy Project!
If you are not sure about the election process, or the expectations of the role, we encourage you
to look over APE0 (https://github.com/astropy/astropy-APEs/blob/main/APE0.rst#the-voting-members).
Being a voting member principally means agreeing to vote in Astropy elections, which occur at most
a few times per year (i.e. this is not a serious time commitment on top of your existing role(s)
within the project).

If you wish to accept this nomination, please respond to this email indicating whether you would
like to accept this nomination. If you do accept the nomination, please write a few sentence
description of your contributions to the Astropy Project that demonstrates the points defined
in APE0 (https://github.com/astropy/astropy-APEs/blob/main/APE0.rst#membership) and send them to
the election managers (reply-all to this email). 

If you do not reply by the end of the day \<July 7\>, we will assume you do not wish to accept
this nomination. You can also explicitly decline by responding to this email. 

For the Coordination Committee
\<sender name\>

<hr/>

Subject: Nomination to be an Astropy Coordination Committee Member

Dear \<NOMINEE\>,

Congratulations, you have been nominated to be a new member of the Coordination Committee
(CoCo) for the Astropy Project!  If you are not sure about the election process, or the
expectations of the role, we encourage you to look over APE0
(https://github.com/astropy/astropy-APEs/blob/main/APE0.rst#the-coordination-committee).
Being a CoCo member has a number of responsibilities that are outlined in APE0, but feel
free to reach out to current CoCo members with any questions.

Please respond to this email indicating whether you would like to accept or decline
this nomination. If you accept the nomination, you must also post a candidate statement on
the OpenAstronomy Discourse forum. A direct link to start a new post in the Astropy category
with the “Astropy” and “CoCo-Election” tags is: https://community.openastronomy.org/new-topic?title=2022%20CoCo%20Election:Name&category=Astropy&tags=astropy,coco-election .
If you don’t already have an account, you can sign up first and then follow the link to
auto-fill your post. You don’t need to do anything other than posting a candidate statement to
accept this nomination and stand in the election.  Voters will be directed to this candidate
statement at the time of the election. 

To accept the nomination, you must post a candidate statement by the end of the day
\<September 24, 2022\>.

For the Coordination Committee,
\<sender name\>
