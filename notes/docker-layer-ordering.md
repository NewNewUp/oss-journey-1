# Docker layer ordering: the cheapest cache win nobody does

Note: `notes/docker-layer-ordering.md` — one of the debugging notes in this repository.

- Copy dependency manifests and install before copying source — code changes then skip reinstalls.
- One RUN that apt-get updates must also clean lists in the same layer or the image bloats forever.
- .dockerignore is not optional: node_modules in the context turns a 2s build into a 2min upload.
- Multi-stage builds: the runtime stage should never see the build toolchain.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
