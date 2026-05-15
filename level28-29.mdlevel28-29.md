# Bandit Level 28 → Level 29

## What the level wanted

Find the password hidden in the git history of a repository.

## Commands used

```bash
# On Kali
cd /tmp
git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
cd repo
cat README.md
git log
git show a3437bddd447f2d496731658e86b98cbea9d3c98
```

## Solution

Cloned the repo and found the password was hidden as `xxxxxxxxxx`.
Used `git log` to see the commit history and found a commit called
"fix info leak" — meaning someone removed the password.
Used `git show` on the previous commit to see the password before it was removed.

## Password found

4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

## What I learned

- `git log` shows the commit history
- `git show <commit-hash>` shows what changed in a commit
- Deleted data in git is not really gone — it stays in history!
- Always be careful what you commit to git
