# Bandit Level 8 → Level 9

## What the level wanted

Find the only line that appears exactly once in `data.txt`.

## Commands used

```bash
sort data.txt | uniq -u
```

## Solution

Used `sort` to sort all lines alphabetically, then `uniq -u`
to show only lines that appear exactly once.

## Password found

4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

## What I learned

- `sort` sorts lines alphabetically
- `uniq -u` shows only unique lines (appearing once)
- `uniq -c` shows how many times each line appears
- `|` (pipe) sends output of one command to another
