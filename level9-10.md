# Bandit Level 9 → Level 10

## What the level wanted

Find the password in `data.txt` which is a binary file,
next to several `=` characters.

## Commands used

```bash
strings data.txt | grep "=="
```

## Solution

Used `strings` to extract human-readable text from the binary file,
then `grep "=="` to find the line with several `=` characters.

## Password found

FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

## What I learned

- `strings` extracts human-readable text from binary files
- Binary files can't be read with `cat` directly
- Combining `strings` and `grep` is powerful for searching binary files
