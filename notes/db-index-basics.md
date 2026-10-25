# The three indexes almost every slow query needs

Note: `notes/db-index-basics.md` — one of the debugging notes in this repository.

- Index the foreign key you filter and join on — the missing-FK-index is the classic slow query.
- Composite index order matters: equality columns first, range column last.
- Every index slows writes; drop the ones no query plan uses (measure, then drop).
- EXPLAIN before and after; 'added an index' is a hypothesis until the plan changes.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
