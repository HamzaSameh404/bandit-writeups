# Bandit Level 31 → Level 32

## What the level wanted

Push a file called `key.txt` with content `May I come in?`
to the remote git repository.

## Commands used

```bash
cd /tmp
rm -rf repo
git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo
cd repo
echo "May I come in?" > key.txt
git add -f key.txt
git commit -m "add key.txt"
git push
```

## Solution

Cloned the repo, created `key.txt` with the required content,
and pushed it. The server validated the file and returned the password.
Used `-f` with `git add` to force add the file past `.gitignore`.

## Password found

3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K

## What I learned

- `git push` uploads local commits to remote repository
- `.gitignore` can block files from being added
- `git add -f` forces adding ignored files
- Servers can run hooks to validate pushed files
