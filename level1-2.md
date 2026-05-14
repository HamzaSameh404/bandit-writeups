# Bandit Level 1 → Level 2

## What the level wanted

Find the password stored in a file called `-` in the home directory.

## Commands used

```bash
cat ./-
```

## Solution

The file was named `-` which is a special character in Linux.
Using `./` before the filename tells Linux to treat it as a file path.

## Password found

263JGJPfgU6LtdEvgfWU1XP5yac29mFx

## What I learned

- Files with special names like `-` need `./` prefix to be read
- `./` means "current directory" in Linux
- `cat -` means "read from keyboard", but `cat ./-` means "read the file"# Bandit Level 1 → Level 2

## What the level wanted

Find the password stored in a file called `-` in the home directory.

## Commands used

```bash
cat ./-
```

## Solution

The file was named `-` which is a special character in Linux.
Using `./` before the filename tells Linux to treat it as a file path.

## Password found

263JGJPfgU6LtdEvgfWU1XP5yac29mFx

## What I learned

- Files with special names like `-` need `./` prefix to be read
- `./` means "current directory" in Linux
- `cat -` means "read from keyboard", but `cat ./-` means "read the file"
