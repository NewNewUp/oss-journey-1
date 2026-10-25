# git push --force-with-lease: the safety net people disable

Note: `notes/git-push-force-with-lease.md` — one of the debugging notes in this repository.

- --force overwrites the remote ref blindly; a teammate's push in between is silently gone.
- --force-with-lease fails when the remote moved past your last fetch, which is the case that matters.
- Caveat: the lease is your local remote-tracking ref — fetch before force-pushing or the lease is stale.
- Habit: set `git config alias.fpf 'push --force-with-lease'` and never type plain -f again.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
