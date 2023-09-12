# Permissions across the Project

This document describes what access permissions are granted to individuals in
different [roles in the project](https://www.astropy.org/team.html#roles).

Occasional *temporary* write (or higher) permissions may be granted for specific
tasks (for example, a maintainer may be given admin rights to a repo to
configure CI for the first time or similar). Such permissions must be done
temporarily unless prescribed otherwise by this document.

For GitHub, the
[permissions](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization)
are enforced by adding individuals to the GitHub team
matching their role (for example, "Astropy Core Maintainers" or "Astropy
website maintainers" for a core maintainer or the astropy.org team, respectively),
a duty primarily performed at the moment by the Coordination Committee.
Temporary permissions should instead use the "collaborator" feature on Github to
make it clear that these permissions are temporary in nature.

Additionally, the granter of permissions (usually the Coordination Committee)
should send a message to the new recipient of write permissions listing the
responsibilities and expectations that go with this - a template for this email
is available [in this repo](../messages/maintainer_access.md). That message may
contain a prompt for a response, which should be cc-ed/forwarded to
`coordinators[at]astropy.org`.

## Access levels

### Core package maintainers

All maintainers listed for the core package receive *write access* to the
repository via the **Astropy Core Maintainers** GitHub team.

### Coordinated package maintainers

Coordinated package maintainers receive **admin access** to the coordinated
package repositories via the **<package name> maintainers** GitHub team (e.g.,
'astroquery maintainers').

Lower priviledge access (e.g., write, triage) could be assigned to additional
contributors as separate teams (e.g., 'Astroquery Triage').

### Core package release coordinators

Core package release coordinators receive **admin access** to the core
repository, as well as the extension-helpers repository
since releases of those packages may be tightly coupled, as
well as **write access** to the website repository. This is done via the **Core
release maintainers** GitHub team.

### Coordination committee

The Coordination Committee members receive **owner access** to
the astropy GitHub organization. Members who are not familiar or
comfortable with GitHub administration may opt out. However,
a majority of the committee should have access. If necessary,
members should receive GitHub administration training before given access.

In addition, they have access to the project
credentials (or the shared password manager to access the credentials).
As with GitHub access above, members may opt out but the majority and training
rules also apply here.

Regardless of access level, the members are always bound by
[APE 0](https://github.com/astropy/astropy-APEs/blob/main/APE0.rst).
For example, a Coordination Committee member cannot delete or transfer
a repository without first obtaining concensus from the community.

## Other ways to gain access

Besides the process laid out a the beginning of this document,
which might not cover all cases, other ways include:

### Automated access

We have an automated workflow to
[invite organization members based on merged PRs](https://github.com/astropy/astropy-tools/actions/workflows/update_org_members.yml).
However, we are open to suggestions on how to improve it
over at [astropy-tools GitHub Issue 178](https://github.com/astropy/astropy-tools/issues/178).

### Manual request

If for some reason there was an oversight in the process or a special
situation that is not covered, people could request access
(for themselves or others) using the
[Astropy Github Organisation Administration](https://github.com/astropy/astropy-project/issues/new?assignees=&labels=github-admin&projects=&template=github-admin.yaml)
issue template. Please clearly state the reason for the request.
Once the issue is opened, one of the Coordination Committee members
would handle it as appropriate.

## Removing access

As people switch roles or leave the project completely, GitHub access
would be adjusted accordingly. For example, if a maintainer is no
longer active and is not responsive to developer surveys,
the Coordination Committee has the right to remove this person
from a named role and thus the associated GitHub permission(s).
This also applies to Coordination Commitee members that rotated off.

Anyone that abuses their given priviledge will also have it removed.
Please report any abuse to the Coordination Committee or the Ombudsperson,
as you see fit.
