# Bandit Level 32 → Level 33

## What the level wanted

Escape from an UPPERCASE shell that converts everything to uppercase.

## Commands used

```bash
$0
cat /etc/bandit_pass/bandit33
```

## Solution

The shell converts everything to uppercase so normal commands fail.
Used `$0` which is a special variable that refers to the current
shell — it spawned a normal `sh` shell that accepts lowercase commands.

## Password found

tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0

## What I learned

- `$0` is a special variable that contains the name of the current shell
- It can be used to spawn a new shell
- UPPERCASE shells are a common CTF escape challenge
- Special variables like `$0` don't get converted to uppercase
