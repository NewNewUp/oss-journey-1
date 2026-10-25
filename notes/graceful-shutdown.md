# Graceful shutdown: drain before you die

Note: `notes/graceful-shutdown.md` — one of the debugging notes in this repository.

- Catch SIGTERM, stop accepting new work, finish in-flight requests, then exit within the timeout.
- Kubernetes kills at the termination grace period; jobs that ignore it get SIGKILLed mid-write.
- Readiness probes should flip false immediately on shutdown so load balancers drain you first.
- Idempotent handlers make imperfect drains harmless.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
