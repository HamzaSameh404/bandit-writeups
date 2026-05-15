# Bandit Level 15 → Level 16

## What the level wanted

Submit the current password to port 30001 on localhost
using SSL/TLS encryption.

## Commands used

```bash
echo "8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo" | openssl s_client -connect localhost:30001 -quiet
```

## Solution

Used `openssl s_client` to connect to port 30001 with SSL/TLS
encryption and sent the current password.

## Password found

kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

## What I learned

- SSL/TLS encrypts the connection between client and server
- `nc` sends data without encryption
- `openssl s_client` connects using SSL/TLS encryption
- This is how HTTPS works on websites
- `-quiet` hides extra SSL handshake information
