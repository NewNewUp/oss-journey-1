# Small, frequent dependency upgrades beat annual big-bangs

Note: `notes/dependency-upgrade.md` — one of the debugging notes in this repository.

- Monthly upgrade PRs stay reviewable; a year of drift is a rewrite.
- Read the changelog of direct dependencies; transitive breakage surfaces in CI, not in notes.
- Upgrade PRs get the same CI gate as feature PRs — no skipping tests for 'just a version bump'.
- Pin toolchain versions in CI to match local dev, or the upgrade works for exactly one person.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
