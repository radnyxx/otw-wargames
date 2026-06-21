# Bandit Level 6 → 7

## Objective
Find a file somewhere on the *entire* filesystem (not just the home directory), identified
by owner (`bandit7`), group (`bandit6`), and size (33 bytes).

## Commands Used
- `find`
- `cat`

## The Logic
This extends the previous level's filtering approach to a system-wide search starting from
`/`. Because many directories aren't readable by this user, the search throws a lot of
"Permission denied" noise — redirecting stderr to `/dev/null` keeps the output clean so the
one real match isn't lost in the clutter.

## The Command
```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat <path_returned_by_find>
```

**Result:** password obtained (redacted).
