# Branch protection: the three rules that stop most incidents

Note: `notes/branch-protection.md` — one of the debugging notes in this repository.

- Require the CI check to pass before merge — self-merge with red CI is how regressions ship.
- Require linear history if you ever bisect; merge commits make `git bisect` noisy.
- Allow admins to bypass is a config most repos should turn off.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
