# CI cache keys: how one bad wheel poisons every later build

Note: `notes/ci-cache-poisoning.md` — one of the debugging notes in this repository.

- Cache keyed only on lockfile hash: a yanked dependency version still resolves and poisons the cache.
- Include the runner OS and toolchain version in the key — a glibc upgrade changes wheel compatibility.
- Always keep a manual cache-bust escape hatch (a workflow_dispatch input that appends a nonce).
- A corrupted cache is invisible: builds stay green while shipping stale artifacts.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
