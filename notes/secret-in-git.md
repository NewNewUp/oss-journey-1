# A secret in git history is compromised, full stop

Note: `notes/secret-in-git.md` — one of the debugging notes in this repository.

- Removing a file in a later commit does nothing; history keeps it until a force-push rewrite.
- Rotate first, clean history second — rotation is the fix, history rewriting is cosmetic.
- Pre-commit secret scanners catch the typos; the big leak is the .env you 'temporarily' committed.
- CI logs print env vars on failure — mask them before the pipeline, not after the leak.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
