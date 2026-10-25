# Every shell script starts with set -euo pipefail

Note: `notes/shell-scripts-set-e.md` — one of the debugging notes in this repository.

- Without -e, a failed cd means the rest of the script runs in the wrong directory.
- -u catches typo'd variables that silently expand to empty strings.
- pipefail stops the classic 'curl | jq' hiding an HTTP 500.
- Quote every expansion; test with a directory containing spaces.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
