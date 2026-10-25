# Flaky tests: quarantine them, never delete them

Note: `notes/flaky-test-quarantine.md` — one of the debugging notes in this repository.

- Deleting a flaky test loses the regression it once caught; quarantine keeps it visible.
- Auto-retry in CI hides flakiness instead of fixing it — retry counts belong in the report, not silently.
- Tag flaky tests with an owner and a review date; unowned quarantines rot.
- Most flakes are shared state: temp dirs, ports, time zones, or test ordering.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
