# Bandit Level 9 → 10

## Objective
Find a password embedded inside a file that's mostly binary/non-printable data, where the
password itself is preceded by several consecutive `=` characters.

## Commands Used
- `strings`
- `grep`

## The Logic
`strings` scans a binary file and prints only the contiguous runs of printable characters,
filtering out the noise of raw binary bytes. Piping that into `grep` for the known marker
pattern (a run of equals signs) narrows the output to the one line that actually matters.

## The Command
```bash
strings data.txt | grep "=="
```

**Result:** password obtained (redacted).
