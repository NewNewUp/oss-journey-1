# HTTP status codes: the five that cover 95% of APIs

Note: `notes/http-status-choice.md` — one of the debugging notes in this repository.

- 200 with a body, 201 with a Location, 400 for malformed input, 401 vs 403 (who are you vs no), 404 for silent resources.
- 500 means 'our fault' — stop returning it for user errors; that pages the wrong team.
- 422 exists for syntactically valid but semantically wrong payloads.
- Consistency inside one API beats correctness against the RFC.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
