# Pagination: offset breaks, cursor scales

Note: `notes/api-pagination.md` — one of the debugging notes in this repository.

- OFFSET scans and skips; page 10,000 is page 1 with extra steps and a hot database.
- Cursor pagination needs a stable, unique, indexed sort key — created_at + id is the usual pair.
- Always cap page size server-side; client-requested 10,000-row pages are a DoS with paperwork.
- Return a next-cursor token; clients computing their own cursors couples them to your schema.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
