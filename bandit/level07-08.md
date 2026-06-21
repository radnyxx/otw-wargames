# Bandit Level 7 → 8

## Objective
Extract the password from a large text file, where it appears next to a specific known
marker word among thousands of irrelevant lines.

## Commands Used
- `grep`
- `cat`

## The Logic
Rather than scrolling through a huge file by eye, `grep` filters for lines containing a
specific keyword, instantly isolating the one relevant line out of thousands.

## The Command
```bash
grep "millionth" data.txt
```

**Result:** password obtained (redacted).
