# Bandit Level 27 → Level 28

## What the level wanted

Clone a git repository and find the password inside it.

## Commands used

```bash
# On Kali (not from the server)
cd /tmp
git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo
cd repo
cat README
```

## Solution

Cloned the git repository from Kali directly since localhost
connections were blocked on the server. Found the password in README.

## Password found

Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

## What I learned

- `git clone` downloads a remote repository
- Git repositories can be hosted over SSH
- Sometimes you need to clone from outside the server
- README files often contain important information
