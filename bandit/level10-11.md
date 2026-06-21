# Bandit Level 10 → 11

## Objective
Decode a password that has been Base64-encoded and stored in a file.

## Commands Used
- `base64`
- `cat`

## The Logic
Base64 is an encoding, not encryption — it's reversible with no key required. The `base64`
utility's `-d` (decode) flag converts the encoded text straight back to its original form.

## The Command
```bash
base64 -d data.txt
```

**Result:** password obtained (redacted).
