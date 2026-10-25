# Using an AI pair: you review, it types

Note: `notes/pairing-with-ai.md` — one of the debugging notes in this repository.

- Generated code is a draft: tests first, then read the diff line by line like any contributor's.
- AI is strongest on boilerplate and weakest on your codebase's invariants — feed it those invariants.
- Never commit code you cannot explain in the PR description; that is the reviewability bar.
- Keep the interesting failures: they make the best debugging notes (like this repository).

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
