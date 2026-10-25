# Type hints pay rent at the call site, not the definition

Note: `notes/type-hints-python.md` — one of the debugging notes in this repository.

- The annotation on a function signature documents and checks every caller at once.
- Run mypy/pyright in CI with the same strictness everywhere; per-file ignores accumulate.
- Typed dicts/protocols beat dicts-of-dicts — the bug class disappears at review time.
- Any is a unlock door: mark it loudly or it spreads.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
