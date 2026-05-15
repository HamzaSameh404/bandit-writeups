# Bandit Level 19 → Level 20

## What the level wanted

Use the setuid binary to read the password as bandit20.

## Commands used

```bash
ls -la
./bandit20-do cat /etc/bandit_pass/bandit20
```

## Solution

Found a setuid binary `bandit20-do` that runs commands as bandit20.
Used it to read the password file that only bandit20 can access.

## Password found

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

## What I learned

- Setuid binaries run as their owner, not the user who runs them
- `s` in permissions `-rwsr-x---` means setuid is set
- Setuid allows privilege escalation in a controlled way
- This is a common concept in Linux security
