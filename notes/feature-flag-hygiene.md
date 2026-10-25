# Feature flags rot: delete the dead ones

Note: `notes/feature-flag-hygiene.md` — one of the debugging notes in this repository.

- Every flag doubles the test matrix; an unused flag is untested code that still ships.
- Record the creation date and owner in the flag name or registry; flags without owners live forever.
- Remove the flag in the same release train that made it permanent — 'later' means never.
- Default-off flags still run their code paths in every deploy; dead branches are not free.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
