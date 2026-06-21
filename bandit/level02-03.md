# Bandit Level 2 → 3

## Objective
Read a file whose name contains spaces, which breaks naive `cat filename` usage since the
shell splits unquoted arguments on whitespace.

## Commands Used
- `ls`
- `cat`

## The Logic
A filename like `spaces in this filename` is seen by the shell as multiple separate
arguments unless it's quoted or escaped. Wrapping the filename in quotes (or escaping each
space with a backslash) tells the shell to treat it as a single token.

## The Command
```bash
ls -la
cat "spaces in this filename"
```

**Result:** password obtained (redacted).
