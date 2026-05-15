# Bandit Level 24 → Level 25

## What the level wanted

A daemon is listening on port 30002.
It gives the bandit25 password only if you send
the bandit24 password + the correct 4 digit PIN.
The PIN is unknown so we had to brute force all 10000 combinations.

## Commands used

```bash
mkdir /tmp/brute24
nano /tmp/brute24/brute.sh
chmod +x /tmp/brute24/brute.sh
/tmp/brute24/brute.sh
```

## Solution

Wrote a bash script that generates all combinations from 0000 to 9999.
Piped all combinations to nc localhost 30002.
The daemon responded with the password when the correct PIN was found.

## Password found

iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

## What I learned

- Brute force means trying all possible combinations automatically
- `seq -w 0000 9999` generates numbers with leading zeros
- Piping a loop into nc sends all output to a network port
- A 4 digit PIN has only 10000 combinations - very easy to brute force
- Always use scripts to automate repetitive tasks
