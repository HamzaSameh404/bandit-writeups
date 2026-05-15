# Bandit Level 25 → Level 26

## What the level wanted

Login as `bandit26` even though its shell is not `/bin/bash`.

## Commands used

```bash
cat bandit26.sshkey
chmod 600 bandit26.sshkey
ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
```

Inside vim:

```vim
:set shell=/bin/bash
:shell
```

Then:

```bash
cat /etc/bandit_pass/bandit26
```

## Solution

The user `bandit26` was using a restricted shell instead of bash.

First, I copied the SSH private key from the server and saved it locally on Kali Linux.
After giving the key the correct permissions using `chmod 600`, I connected using SSH.

The shell automatically opened the `more` program and exited quickly.
To prevent that, I resized the terminal window to a very small height so `more` stayed open.

Inside `more`, I pressed `v` to open `vim`.

From inside `vim`, I escaped into a real bash shell using:

`:set shell=/bin/bash`

Then:

`:shell`

After getting shell access as `bandit26`, I read the password file.

## Password found

```text
s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
```

## What I learned

- Some Linux users can have restricted shells
- `more` can be abused to access `vim`
- `vim` supports shell execution
- Terminal size can affect program behavior
- Shell escape is a common Linux privilege escalation technique
- SSH private keys can be used instead of passwords
