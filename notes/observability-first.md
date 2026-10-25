# Add the log line before the debugger

Note: `notes/observability-first.md` — one of the debugging notes in this repository.

- Three structured fields (id, operation, duration) answer most 'what happened' questions without a repro.
- Correlation ids turn five support tickets into one investigation.
- Metrics for rates, logs for details, traces for paths — reach for them in that order.
- Every alert must link to a runbook; unactionable alerts train people to ignore alerts.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
