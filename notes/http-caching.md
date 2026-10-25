# HTTP caching headers: the cheapest performance work

Note: `notes/http-caching.md` — one of the debugging notes in this repository.

- Cache immutable assets forever (max-age=31536000, immutable) with a content hash in the name.
- HTML and API responses: no-cache + ETag gives revalidation without full downloads.
- A wrong Cache-Control is worse than none — stale auth pages and mixed users are hard to debug.
- Test with curl -I, not by refreshing the browser; caches lie to your eyes.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
