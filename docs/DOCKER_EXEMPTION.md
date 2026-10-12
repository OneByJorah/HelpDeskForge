# Docker exemption — HelpDeskForge

**Status:** Documented exemption from the "every active repository must support containers" requirement.

**Reason:** CSS-only osTicket theme. There is no application runtime to containerize; the theme is installed into an existing osTicket installation via deploy.sh. Containerizing the theme alone would not produce a runnable service.

**Conclusion:** A Dockerfile and docker-compose.yml are not applicable to this repository.
This file records the exemption so the fleet audit has a written exception on file,
as required by the OneByJorah modernization directive "Definition of Done" clause:

> A repository is complete only when every checklist item passes OR a written exception
> exists explaining why a requirement does not apply.

**Exemption owner:** @OneByJorah
**Last reviewed:** 2026-10-12
