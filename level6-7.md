# Bandit Level 6 → Level 7

## What the level wanted

Find the password somewhere on the server in a file with these properties:

- Owned by user bandit7
- Owned by group bandit6
- 33 bytes in size

## Commands used

```bash
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
cat /path/to/file
```

## Solution

Used `find` from root `/` to search the whole server.
Added `-user` and `-group` flags to filter by ownership.
Used `2>/dev/null` to hide permission denied errors.

## Password found

morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

## What I learned

- `find /` searches the entire server
- `-user` and `-group` filter files by ownership
- `2>/dev/null` hides error messages
- `2>` redirects error output, `/dev/null` throws it away
