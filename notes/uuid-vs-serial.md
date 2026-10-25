# UUIDs vs auto-increment: pick per table, not per project

Note: `notes/uuid-vs-serial.md` — one of the debugging notes in this repository.

- Auto-increment leaks volume and collides across shards; UUIDs hide both at a cost of size and index locality.
- UUIDv7 (time-ordered) fixes most index-locality pain of v4.
- External identifiers and internal keys can differ: expose UUIDs, keep a dense internal key for joins.
- Never encode authorization decisions in ID unpredictability; that is what ACLs are for.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
