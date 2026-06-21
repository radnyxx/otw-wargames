# Bandit Level 14 → 15

## Objective
Submit the current level's password to a listening service on localhost port 30000,
which responds with the next level's password if the submitted value is correct.

## Commands Used
- `nc`

## The Logic
This level is about basic raw TCP interaction rather than file/permission tricks. A
service is listening on a given port expecting plaintext input; `nc` (netcat) opens a
direct connection to that port and lets you send the password as a line of input,
printing back whatever the server responds with.

## The Command
```bash
nc localhost 30000
# (paste the current level's password obtained earlier, then press Enter)
```

**Result:** password obtained (redacted).
