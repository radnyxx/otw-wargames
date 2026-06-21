# Bandit Level 12 → 13

## Objective
Recover a password from a file that's a hex dump of data which has been compressed and
archived multiple times in succession, using a mix of formats.

## Commands Used
- `xxd`
- `file`
- `gzip` / `bzip2` / `tar` (as needed, depending on what `file` reports at each step)
- `mkdir`, `cp`, `mv`

## The Logic
The original file is a `xxd`-style hex dump of binary data, so the first step is reversing
that with `xxd -r` to get actual binary back. From there, the binary turns out to be a
compressed/archived blob — but the type isn't given up front. The repeatable strategy is:
run `file` on the current artifact to learn what it actually is (gzip, bzip2, tar, etc.),
rename/extract accordingly, and repeat until `file` reports plain ASCII text. Working in a
scratch directory (e.g. under `/tmp`) avoids cluttering the home directory through several
rounds of extraction.

## The Command
```bash
mkdir /tmp/scratch12 && cd /tmp/scratch12
cp ~/data.txt .
xxd -r data.txt > data.out

# Loop: check type, rename with matching extension, decompress/extract, repeat
file data.out
mv data.out data.gz   # example — actual extension depends on file's output
gzip -d data.gz
file data             # repeat file -> rename -> extract until ASCII text appears
```

**Result:** password obtained (redacted).
