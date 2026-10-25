# Delete dead code; git remembers it so you do not have to

Note: `notes/dead-code-deletion.md` — one of the debugging notes in this repository.

- Commented-out code is noise with a half-life; the VCS is the archive.
- Dead code still costs: it compiles, it confuses grep, it gets 'fixed' when it breaks.
- Delete behind a tag if you are nervous — a tag is cheaper than a comment.
- Coverage tools find unreachable code faster than code review.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
