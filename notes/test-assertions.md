# Assert on behavior, not on implementation details

Note: `notes/test-assertions.md` — one of the debugging notes in this repository.

- Asserting an internal call count breaks every refactor; assert the observable output.
- One logical assertion per test keeps failure messages actionable.
- Test names are specifications: 'rejects expired tokens' beats 'test_auth_3'.
- If a test needs a comment explaining what it checks, the test is wrong.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
