# The logging mistake in every PR review: print in a library

Note: `notes/python-logging-mistake.md` — one of the debugging notes in this repository.

- Libraries must never configure logging; they must only emit through `logging.getLogger(__name__)`.
- print() bypasses severity levels and breaks every aggregator that parses stderr.
- f-strings in log calls format eagerly — use lazy %s args so disabled levels cost nothing.
- exception logging: `log.exception(...)` inside except, or you lose the traceback.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
