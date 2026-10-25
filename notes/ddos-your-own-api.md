# Your own integration tests can DDoS your own API

Note: `notes/ddos-your-own-api.md` — one of the debugging notes in this repository.

- Suite-level rate limiting: parallel test files multiply into hundreds of requests per second.
- Mock external APIs at the network boundary in unit tests; reserve live calls for one nightly job.
- A staging environment with prod-like limits is the only honest test of retry logic.
- Record your test suite's request count; watch it when adding test files.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
