# Bandit Level 17 → Level 18

## What the level wanted

Find the only line that changed between `passwords.old`
and `passwords.new`.

## Commands used

```bash
diff passwords.old passwords.new
```

## Solution

Used `diff` to compare the two files. The line marked
with `>` is the new/changed line which contains the password.

## Password found

x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

## What I learned

- `diff` compares two files and shows the differences
- Lines with `<` are from the first file (old)
- Lines with `>` are from the second file (new)
- `diff` is very useful for finding changes in files
