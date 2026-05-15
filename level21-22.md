# Bandit Level 21 → Level 22

## What the level wanted

A program is running automatically via cron (time-based job scheduler).
We needed to find what script is being run and what it does.

## Commands used

```bash
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
```

## Solution

Found a cronjob running every minute as bandit22.
Read the script and it was writing the bandit22 password to a file in /tmp.
Read that file to get the password.

## Password found

tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

## What I learned

- Cron is a time-based job scheduler in Linux
- Cronjob configs are stored in /etc/cron.d/
- `* * * * *` means the job runs every minute
- Scripts running as another user can expose their passwords
- Always check what automated scripts are doing on a system
