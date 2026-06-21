# Bandit Level 8 → 9

## Objective
A file contains many lines, all duplicated except for exactly one unique line — that
unique line is the password.

## Commands Used
- `sort`
- `uniq`

## The Logic
`uniq` only collapses duplicate lines that are *adjacent* to each other, so the file has
to be sorted first to group identical lines together. Once sorted, `uniq -u` prints only
the lines that have no duplicates at all — which, by the problem's construction, leaves
exactly one line.

## The Command
```bash
sort data.txt | uniq -u
```

**Result:** password obtained (redacted).
