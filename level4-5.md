# Bandit Level 4 → Level 5

## What the level wanted

Find the password in the only human-readable file
inside the `inhere` directory among 10 files.

## Commands used

```bash
cd inhere
file ./*
cat ./-file07
```

## Solution

Used `file ./*` to check the type of every file.
Only `-file07` was ASCII text, the rest were binary data.

## Password found

4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## What I learned

- `file` command tells you the type of a file
- Human-readable files are called ASCII text
- Binary files show as data with the `file` command
- `./*` means all files in the current directory
