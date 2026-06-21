# OverTheWire Write-ups

Personal methodology notes from working through [OverTheWire](https://overthewire.org/wargames/) wargames.

## Purpose

This repo is **not** a list of answers. Passwords and flags are intentionally omitted in
every write-up — each level simply notes that the password was obtained. The goal here is
to document *process*: which tools were used, why, and how the reasoning unfolded level to
level. That's what's actually useful to show employers, mentors, or your future self.

## Ethics Note

OverTheWire explicitly asks players not to publish passwords or step-by-step "just run this"
walkthroughs, since that spoils the challenge for others. In line with that:

- No passwords or flags appear anywhere in this repo.
- Write-ups explain *concepts* (permissions, encoding, process inspection, etc.) rather than
  handing over copy-paste solutions.
- Where a command would reveal a password as part of its normal output, the output is shown
  with the password redacted or simply described.

If you're working through Bandit yourself, I'd encourage you to use these as a check on your
own thinking after you've already tried the level — not as a shortcut.

## Structure

```
bandit/
  level00-01.md
  level01-02.md
  level02-03.md
  ...
  level15-16.md
```

Each file is named `levelN-M.md`, where `N` is the level you start on and `M` is the level
the password gets you into.

## Format

Every write-up follows the same template:

- **Objective** — what the level is asking you to do
- **Commands Used** — the tools involved
- **The Logic** — short explanation of the vulnerability/technique/reasoning
- **The Command** — the actual command(s) run, with sensitive output redacted

## Progress

- [x] Bandit: level0 → level16

## Disclaimer

These notes reflect my own work solving each level. They're shared for learning purposes only.
Please don't use this repo to skip the productive struggle of OverTheWire — that struggle is
the entire point.
