# Respect Retry-After or the rate limiter owns you

Note: `notes/rate-limit-backoff.md` — one of the debugging notes in this repository.

- 429 responses tell you when to come back; ignoring them upgrades a soft block to a ban.
- Global budgets (a token bucket per API key) beat per-call sleeps.
- Differentiate 429 (back off, retry) from 5xx (back off, retry, and alert) from 4xx (do not retry).
- Persist retry state across process restarts or a crash re-triggers the storm.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
