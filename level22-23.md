# Bandit Level 22 → Level 23

## What the level wanted

A cronjob is running automatically as bandit23.
The script creates a hashed filename and stores the password there.
We needed to reverse-engineer the script to find where the password is.

## Commands used

```bash
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```

## Solution

Read the cronjob script and understood it was hashing "I am user bandit23" with md5.
Ran the same command ourselves to get the hash.
Used that hash as the filename to read the password from /tmp.

## Password found

0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

## What I learned

- md5sum converts any text into a unique fixed hash
- Scripts can use hashes as filenames to obscure file locations
- If you understand the logic of a script you can replicate it
- cut -d ' ' -f 1 takes the first part before a space
