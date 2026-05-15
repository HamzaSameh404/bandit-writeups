# Bandit Level 20 → Level 21

## What the level wanted

There is a setuid binary called `suconnect` in the home directory.
It connects to a port on localhost that we specify.
If it finds the bandit20 password there, it sends back the bandit21 password.

## Commands used

```bash
echo "0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO" | nc -l -p 4444 &
./suconnect 4444
```

## Solution

Set up a netcat listener in the background on port 4444 serving the bandit20 password.
Then ran suconnect pointing to port 4444 — it verified the password and returned bandit21's password.

## Password found

EeoULMCra2q0dSkYj561DX7s1CpBuOBt

## What I learned

- `nc -l -p <port>` opens a listener on a port
- `&` runs a process in the background so you can keep typing
- You can pipe data into netcat to serve it to anyone who connects
- Two processes can communicate with each other via localhost ports
- setuid binaries can verify credentials over a network socket
