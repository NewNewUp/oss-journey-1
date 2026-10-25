# Every network call needs a timeout, no exceptions

Note: `notes/timeout-everywhere.md` — one of the debugging notes in this repository.

- A client without a timeout hangs forever on a dropped packet; the default is almost always infinite.
- Set connect and read timeouts separately — a fast connect says nothing about slow bodies.
- Retries without deadlines multiply: 3 retries × no timeout = 3 hung threads.
- Propagate deadlines through the call chain so the outermost budget wins.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
