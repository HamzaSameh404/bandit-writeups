# Bandit Level 12 → Level 13

## What the level wanted

Find the password in `data.txt` which is a hexdump of a file
that has been compressed multiple times.

## Commands used

```bash
mkdir /tmp/hamza123
cp data.txt /tmp/hamza123
cd /tmp/hamza123
xxd -r data.txt > data

# gzip
mv data data.gz
gzip -d data.gz

# bzip2
mv data data.bz2
bzip2 -d data.bz2

# gzip again
mv data data.gz
gzip -d data.gz

# tar
mv data data.tar
tar -xf data.tar

# tar again
tar -xf data5.bin

# bzip2 again
mv data6.bin data6.bz2
bzip2 -d data6.bz2

# tar again
tar -xf data6

# gzip again
mv data8.bin data8.gz
gzip -d data8.gz

cat data8
```

## Solution

Converted hexdump to binary with `xxd -r`, then kept checking
the file type with `file` and decompressing until we got ASCII text.

## Password found

FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

## What I learned

- `xxd -r` converts a hexdump back to binary
- `gzip -d` decompresses gzip files
- `bzip2 -d` decompresses bzip2 files
- `tar -xf` extracts tar archives
- `file` command is essential to know what to do next
- Files can be compressed multiple times!
