# Bandit Level 14 → Level 15

## What the level wanted

Submit the current level's password to port 30000 on localhost
to get the next password.

## Commands used

```bash
echo "MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS" | nc localhost 30000
```

## Solution

Used `nc` (netcat) to connect to port 30000 on localhost and
sent the current password. The server responded with the next password.

## Password found

8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

## What I learned

- Ports are like doors on a server, each serving a different purpose
- `nc` (netcat) connects to any port on a server
- `echo "text" | nc` sends text to a port
- Common ports: 22=SSH, 80=HTTP, 443=HTTPS
