# Bandit Level 5 → 6

## Objective
Locate one specific file buried in a large nested directory tree, identified by three
known attributes: human-readable, exactly 1033 bytes, and not executable.

## Commands Used
- `find`
- `cat`

## The Logic
With dozens of nested directories and files, manual searching doesn't scale. `find` lets
you filter by multiple file attributes simultaneously — size, permission bits, type — in
a single pass over the whole tree, which narrows a huge search space down to one match.

## The Command
```bash
find . -type f -size 1033c ! -perm /111
cat <path_returned_by_find>
```

**Result:** password obtained (redacted).
