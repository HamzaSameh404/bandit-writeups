# Bandit Level 11 → Level 12

## What the level wanted

Find the password in `data.txt` where all letters are rotated by 13 positions (ROT13).

## Commands used

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

## Solution

Used `tr` to translate each letter by shifting it 13 positions.
ROT13 means A→N, B→O, and so on.

## Password found

7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

## What I learned

- ROT13 is a simple cipher that shifts each letter by 13 positions
- `tr` command translates/replaces characters
- ROT13 applied twice gives you the original text
- This is encoding NOT encryption — very easy to decode
