# Bandit Level 13 → Level 14

## What the level wanted

Login as bandit14 using a private SSH key instead of a password,
then read the password from `/etc/bandit_pass/bandit14`.

## Commands used

```bash
# On Kali - copy the key from the server
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private ~/sshkey.private

# Fix permissions
chmod 600 ~/sshkey.private

# Connect as bandit14 using the key
ssh -i ~/sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

# Read the password
cat /etc/bandit_pass/bandit14
```

## Solution

Downloaded the private SSH key using `scp`, fixed its permissions
with `chmod 600`, then used it to login as bandit14 with `ssh -i`.

## Password found

MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

## What I learned

- SSH keys are used instead of passwords for authentication
- `scp` copies files between machines over SSH
- `chmod 600` sets file permissions to owner-only read/write
- `ssh -i` tells SSH to use a specific key file
