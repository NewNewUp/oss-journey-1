# Commit the lockfile — except when you are a library

Note: `notes/lockfile-commit.md` — one of the debugging notes in this repository.

- Applications commit lockfiles for reproducible builds; libraries usually omit them.
- A lockfile drift check in CI catches accidental hand-edits and partial upgrades.
- Regenerating a lockfile in a PR is a separate commit, or review becomes impossible.
- Pin the package manager version too; lockfiles are not portable across major versions.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
