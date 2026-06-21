# Bandit Level 11 → 12

## Objective
Decode a password that has been obfuscated with a ROT13 substitution cipher (each letter
shifted 13 places through the alphabet).

## Commands Used
- `tr`
- `cat`

## The Logic
ROT13 is its own inverse — applying the same 13-place shift a second time returns the
original text, since 13 + 13 = 26, a full cycle of the alphabet. `tr` can perform this
shift directly by mapping each letter of the alphabet to the letter 13 positions later
(wrapping around), for both uppercase and lowercase ranges.

## The Command
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

**Result:** password obtained (redacted).
