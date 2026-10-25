# Dev-prod parity: the differences you forget are the outages you get

Note: `notes/local-dev-parity.md` — one of the debugging notes in this repository.

- Different databases (SQLite in dev, Postgres in prod) hide dialect bugs until demo day.
- Time, filesystem case-sensitivity, and locales differ on laptops; CI on Linux is not enough.
- Containers make parity cheap; a compose file is documentation that runs.
- Seed dev data shaped like prod data, or queries tuned to toy data fail at scale.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
