# Config precedence: write it down or debug it forever

Note: `notes/config-precedence.md` — one of the debugging notes in this repository.

- Define one order (flag > env > file > default) and enforce it in one place.
- Partial overrides are the bug factory: a half-updated env var set wins in prod and loses in dev.
- Print the effective config (secrets redacted) at startup; support tickets end at that log line.
- Hot-reload is a feature you must test; most stacks should not have it.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
