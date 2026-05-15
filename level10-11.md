# Bandit Level 10 → Level 11

## What the level wanted

Find the password in `data.txt` which contains base64 encoded data.

## Commands used

```bash
base64 -d data.txt
```

## Solution

Used `base64 -d` to decode the base64 encoded data in the file.

## Password found

dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## What I learned

- Base64 is a way to encode binary data into readable text
- Base64 encoded text usually ends with `=` or `==`
- `base64 -d` decodes base64 data back to normal text
- Encoding is NOT encryption — anyone can decode it!
