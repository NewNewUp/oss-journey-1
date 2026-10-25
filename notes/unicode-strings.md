# Unicode: the length of a string is a lie

Note: `notes/unicode-strings.md` — one of the debugging notes in this repository.

- len() counts code points; users count glyphs; databases count bytes. Three different answers.
- Normalize (NFC) on input or 'café' and 'café' are different keys in your dict.
- Test with emoji, Turkish dotless i, and CJK — ASCII-only test suites pass and prod breaks.
- File names, slugs, and IDs have different Unicode rules; do not reuse one sanitizer for all.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.
