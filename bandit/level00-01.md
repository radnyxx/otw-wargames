# Bandit Level 0 → 1

## Objective
Connect to the Bandit game server over SSH using the publicly known starting
credentials and locate the password for the next level.

## Commands Used
- `ssh`
- `cat`
- `ls`

## The Logic
Level 0 doesn't require exploitation — it's the entry point and just confirms you can
authenticate to the host on the documented port. Once connected, the password for the
next level is sitting in the home directory as a plain file. The only "skill" here is
knowing to check your home directory contents immediately after login and read whatever
is in there.

## The Command
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
# (authenticate with the level0 password published on the OverTheWire site)

ls
cat readme
```

**Result:** password obtained (redacted).
