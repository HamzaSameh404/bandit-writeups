# Bandit Level 18 → Level 19

## What the level wanted

Read the `readme` file but the shell kicks you out immediately
when you login due to a modified `.bashrc`.

## Commands used

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme"
```

## Solution

Ran `cat readme` directly via SSH without opening a shell,
so the logout in `.bashrc` never had a chance to run.

## Password found

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

## What I learned

- `.bashrc` runs every time you open a shell
- You can run commands directly via SSH without opening a shell
- `ssh user@host "command"` runs a command and exits
- This bypasses any logout traps in `.bashrc`
