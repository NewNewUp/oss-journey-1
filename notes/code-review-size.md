# Review latency is proportional to diff size squared

Note: `notes/code-review-size.md` — one of the debugging notes in this repository.

- PRs over ~400 lines get rubber-stamped; split by behavior, not by file count.
- A PR that fixes and refactors at once is two reviews; separate them.
- Description carries the 'why', the diff carries the 'how', tests carry the 'proof'.
- Small PRs merge fast, and fast merges keep branches from drifting.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
