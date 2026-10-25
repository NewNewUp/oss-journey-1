# Logs without rotation are a disk-full outage on a timer

Note: `notes/log-rotation.md` — one of the debugging notes in this repository.

- Every long-running process needs size- or time-based rotation from day one.
- Structured single-line logs survive rotation and parsing; multi-line stack traces need framing.
- Ship logs out of the box (stdout + collector) rather than managing files on the host.
- Keep debug level off in prod but one flag away — you will need it at 3am.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
