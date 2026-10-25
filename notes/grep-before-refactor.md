# Grep before you refactor: the string-typed world

Note: `notes/grep-before-refactor.md` — one of the debugging notes in this repository.

- Names live in strings: config keys, log fields, URLs, DB columns. grep finds them, the compiler does not.
- Search case-insensitively and across file types (.yml, .md, .sh) before renaming anything.
- External consumers may depend on your 'internal' strings — API paths and env vars are contracts.
- Keep a rename checklist: code, config, docs, dashboards, alerts.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
