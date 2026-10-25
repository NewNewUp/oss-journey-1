# Vendoring dependencies: when 'offline builds' matter

Note: `notes/vendoring-deps.md` — one of the debugging notes in this repository.

- Vendoring pins the world, at the cost of a big diff on every bump — automate the update.
- CI must build with the vendored sources, not network-fetched ones, or the vendor dir is decorative.
- License review gets easier with vendoring: the licenses are physically in your tree.
- Keep a documented escape hatch to unfetchable (network-off) builds for regulated environments.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
