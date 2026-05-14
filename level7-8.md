# Bandit Level 7 → Level 8

## What the level wanted

Find the password in `data.txt` next to the word "millionth".

## Commands used

```bash
grep "millionth" data.txt
```

## Solution

The file had millions of lines so we couldn't read it with `cat`.
Used `grep` to search for the word "millionth" and it printed
only the line containing the password.

## Password found

dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

## What I learned

- `grep` searches for a pattern inside a file
- `grep "word" filename` prints only lines containing that word
- Very useful when files are too large to read manually
