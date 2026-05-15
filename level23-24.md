# Bandit Level 23 → Level 24

## What the level wanted

A cronjob runs every minute as bandit24.
It executes any script in /var/spool/bandit24/foo/ owned by bandit23.
We needed to write our own script to steal bandit24's password.

## Commands used

```bash
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
mkdir /tmp/mybandit24
nano /tmp/mybandit24/getpass.sh
chmod 777 /tmp/mybandit24/getpass.sh
cp /tmp/mybandit24/getpass.sh /var/spool/bandit24/foo/
cat /tmp/mybandit24/password.txt
```

## Solution

Read the cronjob script and understood it runs any script owned by bandit23
in /var/spool/bandit24/foo/ as bandit24.
Wrote a script that copies bandit24's password to /tmp.
Waited one minute for the cronjob to execute it.

## Password found

gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

## What I learned

- Cronjobs can be exploited by placing scripts in the right directory
- chmod 777 makes a file readable and executable by everyone
- Writing scripts that run as another user can expose their files
- Always wait for the cronjob interval before checking results
