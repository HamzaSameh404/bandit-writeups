# Bandit Level 29 → Level 30

## What the level wanted

Find the password hidden in a different git branch.

## Commands used

```bash
# On Kali
cd /tmp
rm -rf repo
git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo
cd repo
cat README.md
git branch -a
git checkout dev
cat README.md
```

## Solution

Cloned the repo and found the password was hidden as
`<no passwords in production!>` in the master branch.
Used `git branch -a` to list all branches and found a `dev` branch.
Switched to it with `git checkout dev` and found the real password.

## Password found

qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

## What I learned

- Git projects can have multiple branches
- `git branch -a` shows all branches including remote ones
- `git checkout` switches between branches
- Developers sometimes leave sensitive data in non-production branches
