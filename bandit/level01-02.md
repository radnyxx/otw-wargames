# Bandit Level 1 → 2

## Objective
Read the contents of a file literally named `-`, which is awkward because most CLI tools
interpret a leading dash as the start of a flag rather than a filename.

## Commands Used
- `cat`
- `ls`

## The Logic
Shells and most Unix tools parse `-` (or anything starting with `-`) as an option flag
when it appears as a bare argument. To force the tool to treat it as a filename instead,
you either give an explicit path (`./-`) or use `--` to tell the program "everything after
this is a positional argument, not a flag."

## The Command
```bash
ls -la
cat ./-
```

**Result:** password obtained (redacted).
