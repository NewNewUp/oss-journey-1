# Test data builders beat 40-line setup blocks

Note: `notes/test-data-builders.md` — one of the debugging notes in this repository.

- A builder with sensible defaults makes the one field under test obvious in the assertion.
- Copy-and-pasted fixtures drift; one builder function keeps tests honest about what matters.
- Randomize irrelevant fields to catch hidden ordering assumptions — but seed for reproducibility.
- Builders belong in test code, never in production packages.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
