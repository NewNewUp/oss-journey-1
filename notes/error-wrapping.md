# Wrap errors with context, but keep the cause

Note: `notes/error-wrapping.md` — one of the debugging notes in this repository.

- A bare `return err` loses the operation; `wrap(err, "opening config")` keeps the chain.
- Never string-format the cause away — future debuggers need `%v` chains, not one flat line.
- Sentinel errors and typed errors both survive wrapping; pick one style per codebase.
- The top of the chain logs; the middle only adds context.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
