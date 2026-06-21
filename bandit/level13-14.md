# Bandit Level 13 → 14

## Objective
Use a provided SSH private key to authenticate as the next level's user, rather than a
password.

## Commands Used
- `ssh`
- `chmod`

## The Logic
This level hands you an RSA private key directly instead of a password. SSH will refuse
to use a private key file if its permissions are too permissive (group/world readable),
as a safety measure against key theft — so the permissions need tightening before it'll
be accepted. From there, it's a normal key-based SSH login pointed at the next user.

## The Command
```bash
chmod 600 sshkey.private
ssh -i sshkey.private bandit14@localhost -p 2220
```

**Result:** password obtained (redacted) — found in the next user's home directory after login.
