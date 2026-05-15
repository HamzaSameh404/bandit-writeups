# Bandit Level 26 → Level 27

## What the level wanted

Get the password for `bandit27` using a SUID binary called `bandit27-do`.

## Commands used

```bash
ls -la
./bandit27-do cat /etc/bandit_pass/bandit27
```

## Solution

After gaining a shell as `bandit26`, I listed the files in the home directory and found an interesting executable called `bandit27-do`.

The file had the SUID bit set (`s`), meaning it runs with the privileges of its owner (`bandit27`) instead of the current user (`bandit26`).

By using this binary, I was able to execute commands as `bandit27`. I used it to read the protected password file:

```bash
./bandit27-do cat /etc/bandit_pass/bandit27
```

## Password found

upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

## What I learned

- What SUID binaries are and how they work
- How privilege escalation can happen in Linux
- How to execute commands with elevated permissions using a helper binary
- Importance of checking file permissions carefully in security challenges
