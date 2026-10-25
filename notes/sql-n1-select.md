# The N+1 that hides behind an ORM's lazy loading

Note: `notes/sql-n1-select.md` — one of the debugging notes in this repository.

- One query per row is invisible in dev (10 rows) and fatal in prod (10k rows).
- Fix with a single IN query or a join; batch loaders beat both for graph-shaped access.
- Measure with query counters in tests — assert an upper bound so the N+1 cannot come back.
- Logging every query in a staging run finds N+1s faster than any profiler.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
