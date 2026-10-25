# CORS is the browser's rule, not the server's defense

Note: `notes/cors-basics.md` — one of the debugging notes in this repository.

- CORS does not protect your API; it protects your users' browsers from other sites.
- Access-Control-Allow-Origin: * is fine for public reads and wrong for anything with cookies.
- Credentials mode requires an exact origin and cannot be a wildcard — configure the allowlist.
- Preflight (OPTIONS) failures look like app bugs; log them distinctly.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
