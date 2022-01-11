# Permissions across the Project

This document describes what access permissions are granted to individuals in
different [roles in the project](https://www.astropy.org/team.html#roles).

Occasional *temporary* write (or higher) permissions may be granted for specific
tasks (for example, a maintainer may be given admin rights to a repo to
configure CI for the first time or similar). Such permissions must be done
temporarily unless prescribed otherwise by this document.

For GitHub, the permissions are enforced by adding individuals to the GitHub team
matching their role (for example, "Astropy Core Maintainers" or "Astropy
website maintainers" for a core maintainer or the astropy.org team, respectively),
a duty primarily performed at the moment by the Coordination Committee.
Temporary permissions should instead use the "collaborator" feature on Github to
make it clear that these permissions are temporary in nature.

Additionally, the granter of permissions (usually the Coordination Committee)
should send a message to the new recipient of write permissions listing the
responsibilities and expectations that go with this - a template for this email
is available [in this repo](../messages/core_write_access.md). That message may
contain a prompt for a response, which should be cc-ed/forwarded to
coordinators@astropy.org

## Core package maintainers

All maintainers listed for the core package receive *write access** to the
repository via the **Astropy Core Maintainers** GitHub team.

## Coordinated package maintainers

Coordinated package maintainers receive **admin access** to the coordinated
package repositories via the **<package name> maintainers** GitHUb team (e.g.,
'astroquery maintainers').

## Core package release coordinators

Core package release coordinators receive **admin access** to the core
repository, as well as the astropy-helpers and extension-helpers repositories
since releases of those packages may be tightly coupled to the core package, as
well as **write access** to the website repository. This is done via the **Core
release maintainers** GitHub team.

## Coordination committee

The coordination committee members receive **owner access** to
the astropy organization. In addition, they have access to the project
credentials (or the shared password manager to access the credentials).
