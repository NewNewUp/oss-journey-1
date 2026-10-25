# Renaming a Go/Py package? Semver still applies to the import path

Note: `notes/semver-importpath.md` — one of the debugging notes in this repository.

- Moving a type breaks every import; keep a type alias in the old location for one minor release.
- Deprecation notes in changelogs are read by nobody — deprecate in code with warnings.
- Major-version bumps in module paths (Go) are the contract; v2 is a different package.
- Grep your own docs for the old path before tagging the release.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
