# Background jobs will run twice; design for it

Note: `notes/background-job-idempotency.md` — one of the debugging notes in this repository.

- At-least-once delivery is the norm; exactly-once is a marketing term for at-least-once + dedup.
- Make the job's effect idempotent (upsert, conditional update), not just its entry point.
- Poison pills need a dead-letter path with alerting, or one bad message blocks the queue.
- Log a correlation id from the trigger to the effect, or debugging async is guesswork.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
