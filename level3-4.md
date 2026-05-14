# Bandit Level 3 → Level 4

## What the level wanted

Find the password in a hidden file inside the `inhere` directory.

## Commands used

```bash
cd inhere
find
cat ./...Hiding-From-You
```

## Solution

Used `find` to list all files including hidden ones.
The hidden file was called `...Hiding-From-You`.

## Password found

2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

## What I learned

- Hidden files in Linux start with a dot `.`
- `ls -la` shows all files including hidden ones
- `find` lists all files and directories recursively
