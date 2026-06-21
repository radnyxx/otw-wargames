# Bandit Level 3 → 4

## Objective
Find a password file hidden inside a subdirectory, where the file itself is a "hidden"
dotfile and won't show up under a default `ls`.

## Commands Used
- `cd`
- `ls -la`
- `cat`

## The Logic
Unix treats any filename starting with a `.` as hidden from a plain `ls` listing. The
`-a` (all) flag is what reveals dotfiles, including the often-overlooked `.` and `..`
directory entries. This level is really just testing whether you know that "no files
here" from a bare `ls` doesn't mean the directory is actually empty.

## The Command
```bash
cd inhere
ls -la
cat ".hidden filename that needed quoting or similar"
```

**Result:** password obtained (redacted).
