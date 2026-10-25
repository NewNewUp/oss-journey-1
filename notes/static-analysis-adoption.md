# Adopting a linter on a legacy repo without a mutiny

Note: `notes/static-analysis-adoption.md` — one of the debugging notes in this repository.

- Enable the rule, then auto-fix and commit once; new violations then fail CI from a clean baseline.
- A baseline file that freezes old violations must have an expiry date, or it becomes permanent.
- Start with correctness rules; style rules first guarantee a format-only PR month.
- Every suppression carries a reason and an issue link.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
