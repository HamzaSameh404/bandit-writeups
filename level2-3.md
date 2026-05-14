# Bandit Level 2 → Level 3

## What the level wanted

Find the password in a file called `--spaces in this filename--`

## Commands used

```bash
ls
cat ./'--spaces in this filename--'
```

## Solution

The file had `--` at the start and end plus spaces inside.
Used single quotes with `./` prefix to handle both the
special characters and spaces in the filename.

## Password found

MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

## What I learned

- Use quotes to handle filenames with spaces
- Use `./` prefix for files with special characters like `--`
- Tab autocomplete helps find tricky filenames
- Single quotes `' '` treat everything inside as literal text
