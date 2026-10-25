# Retries need idempotency, or you send the email twice

Note: `notes/idempotent-retry.md` — one of the debugging notes in this repository.

- Only retry operations that are safe to repeat; annotate or wrap unsafe ones explicitly.
- Idempotency keys turn unsafe retries into safe ones — the server deduplicates.
- Exponential backoff with jitter; thundering herds are real and synchronized retries cause them.
- Count and alert on retries — a rising retry rate is an incident signal, not background noise.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
