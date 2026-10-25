# Store instants in UTC, render in the user's zone

Note: `notes/timezones-storage.md` — one of the debugging notes in this repository.

- A datetime without a timezone is a guess; store UTC + offset-free and convert at the edge.
- Local midnight, DST gaps, and leap days are where date math goes to die — use a real library.
- Never compare naive and aware datetimes; Python throws, SQL silently misorders.
- Schedule jobs with an explicit zone and document the DST behavior you chose.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
