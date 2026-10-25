# Migrations that do not lock: the expand-contract pattern

Note: `notes/db-migration-safety.md` — one of the debugging notes in this repository.

- Adding a nullable column is safe; adding a NOT NULL column on a big table takes a lock that stops the world.
- Expand (add new shape, backfill in batches), deploy readers, then contract (drop old shape) in a later release.
- Every migration gets a rollback statement or an explicit 'no return' note.
- Test migrations against a copy of prod-sized data, not the fixture database.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
