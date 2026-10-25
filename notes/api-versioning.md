# API versioning: pick one scheme and enforce it at the edge

Note: `notes/api-versioning.md` — one of the debugging notes in this repository.

- URL versioning (/v1/) is blunt but debuggable; header versioning is elegant and invisible.
- Never break a shipped version silently — additive fields only, removals get a deprecation window.
- Log the version with every request so you know when v1 traffic actually reaches zero.
- Version the error format too; clients parse errors harder than successes.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
