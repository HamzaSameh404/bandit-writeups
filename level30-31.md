# Bandit Level 30 → Level 31

## What the level wanted

Find the password hidden in a git tag.

## Commands used

```bash
cd /tmp
rm -rf repo
git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
cd repo
cat README.md
git tag
git show secret
```

## Solution

Cloned the repo and found README was empty.
Used `git tag` to list all tags and found one called `secret`.
Used `git show secret` to reveal the password.

## Password found

fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

## What I learned

- Git tags mark specific points in the repository history
- `git tag` lists all tags
- `git show <tag>` shows the content of a tag
- Sensitive data can be hidden in git tags
