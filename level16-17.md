# Bandit Level 16 → Level 17

## What the level wanted

Find which port between 31000-32000 supports SSL, submit the
current password, and get a private SSH key for the next level.

## Commands used

```bash
# Scan for open ports
nmap -sV localhost -p 31000-32000

# Submit password to the correct port
echo "kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx" | openssl s_client -connect localhost:31790 -quiet

# Save the key and fix permissions
nano ~/bandit17.private
chmod 600 ~/bandit17.private

# Connect as bandit17
ssh -i ~/bandit17.private bandit17@bandit.labs.overthewire.org -p 2220

# Read the password
cat /etc/bandit_pass/bandit17
```

## Solution

Used `nmap` to scan ports 31000-32000 and found port 31790
running ssl/unknown. Sent the password to it using openssl
and received a private SSH key. Used the key to login as bandit17.

## Password found

EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

## What I learned

- `nmap -sV` scans ports and detects services
- echo port was sending back the same data (not useful)
- ssl/unknown was the target port
- Private SSH keys can be received as text and saved to a file
- Always `chmod 600` private key files
