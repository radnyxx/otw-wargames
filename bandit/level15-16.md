# Bandit Level 15 → 16

## Objective
Submit the current password to a service on port 30001, except this time the connection
is encrypted with SSL/TLS rather than being plaintext.

## Commands Used
- `openssl`

## The Logic
Plain `nc` can't speak TLS, so connecting directly to this port with netcat just gets a
handshake failure or garbage. `openssl s_client` performs the TLS handshake and then gives
an interactive connection where plaintext can be typed through the now-encrypted channel,
similar in spirit to the previous level but wrapped in encryption.

## The Command
```bash
openssl s_client -connect localhost:30001
# (after the handshake completes, paste the current level's password and press Enter)
```

**Result:** password obtained (redacted).
