# Bandit Level 4 → 5

## Objective
Out of several files in a directory, only one contains human-readable ASCII text — that's
the password file. The rest are decoys with binary or garbage content.

## Commands Used
- `ls`
- `file`
- `cat`

## The Logic
The `file` command inspects a file's actual content/magic bytes rather than trusting its
name or extension, and reports the type (e.g. "ASCII text" vs "data" vs "ELF executable").
Running it against every file in the directory at once quickly narrows down which single
file is plain text and therefore worth `cat`-ing.

## The Command
```bash
cd inhere
file ./*
cat ./-file07   # whichever filename `file` flagged as "ASCII text"
```

**Result:** password obtained (redacted).
