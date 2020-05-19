# Write Permissions for Coordinated Package Repositories

This policy describes the rules and expectations for receiving write permissions for Coordinated Packages (including the Astropy Core Package).

Github write privileges are granted when someone is given a relevant named role. In most cases this is package (or sub-package) maintainer, although other roles (for example, the astropy.org web page maintainer) may also come with write permissions for a specific named repository.  Occasional *temporary* write (or higher) permissions may be grant for specific tasks (for example, a maintainer may be given admin rights to a repo to configure CI for the first time or similar), be such permissions must be done temporarily.

Normal write permissions should be given by assigning sometime to the Github Team that corresponds to that role (For Example, "Astropy Core Maintainers" or "Astropy web site maintainers" for a core maintainer or the astropy.org team, respectively), a duty primarily performed by the Coordination Committee.  Temporary permissions should instead use the "collaborator" feature on Github to make it clear that these permissions are temporary in nature.

Additionally, the granter of permissions (usually the Coordination Committee) should send a message to the new recipient of write permissions the responsibilities and expectations that go with this - a template for this email is available [in this repo](../messages/core_write_access.md). That message may contain a prompt for a response, which should be cced/forwarded to coordinators@astropy.org