# Fail fast on missing environment variables at boot

Note: `notes/env-var-validation.md` — one of the debugging notes in this repository.

- A missing env var discovered at request time is an outage; at boot it is a one-line fix.
- Validate types and shapes once, into a typed config struct — no os.environ reads scattered around.
- Print which variable failed and which docs section explains it; future-you will thank present-you.
- Never log secret values while validating.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
