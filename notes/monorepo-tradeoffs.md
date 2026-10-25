# Monorepos: shared tooling, shared blast radius

Note: `notes/monorepo-tradeoffs.md` — one of the debugging notes in this repository.

- One repo fixes version skew; it also couples every team's CI to every other team's mistakes.
- Path-based CI triggers keep builds fast; without them, a README edit runs the full test matrix.
- Code owners are mandatory above ~10 contributors, or review requests become noise.
- Concrete ownership of shared packages matters more than the repo boundary.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
