# Bandit Level 5 → Level 6

## What the level wanted

Find the password in a file inside `inhere` directory with these properties:

- Human-readable
- 1033 bytes in size
- Not executable

## Commands used

```bash
cd inhere
find . -type f -size 1033c
cat ./maybehere07/.file2
```

## Solution

Used `find` with `-size 1033c` to search for a file with exactly
1033 bytes. Found it at `./maybehere07/.file2` and read it with `cat`.

## Password found

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

## What I learned

- `find -type f` searches for files only
- `find -size 1033c` searches by size (`c` means bytes)
- `find` can search recursively through all subdirectories
- You can combine multiple conditions in one `find` command
