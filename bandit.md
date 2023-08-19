# Over the Wire: Bandit Solutions

Bandit 0: ssh

- `man ssh`: `ssh [user]@[hostname] -p [port]`
- `ssh bandit0@bandit.labs.overthewire.org -p 2220`, password `bandit0`
- Passphrase: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

Bandit 1: ssh, cat

- `ssh` into `bandit1`, repeat this process for future
- `cat ./-`
- Passphrase: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

Bandit 2: cat

- `cat spaces\ in\ this\ filename`
- Passphrase: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

Bandit 3: cat

- `cd inhere/ && ls -a && cat .hidden`
- Passphrase: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

Bandit 4: Find ASCII files

- `cd inhere && file ./*` shows only `-file07` is ASCII
- Passphrase: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

Bandit 5: find

- `cd inhere && find -type f -size 1033c \! -executable | xargs cat`
- Passphrase: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

Bandit 6: find, advanced

- `find / -user bandit7 -group bandit6 -size 33c 2>/dev/null | xargs cat`
  - `2>/dev/null` redirects "Permission Denied" errors
- Passphrase: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

Bandit 7: grep

- `cat data.txt | grep "millionth"`
- Alternate: `awk '/^millionth/ {print $2;}' data.txt`
- Passphrase: TESKZC0XvTetK0S9xNwm25STk5iWrBvP

Bandit 8: Get unique string

- `sort data.txt | uniq -u`
- Passphrase: EN632PlfYiZbn3PhVK3XOGSlNInNE00t

Bandit 9: Find readable strings

- `strings data.txt | grep "^=\+"`
- Passphrase: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

Bandit 10: base64 decoding

- `base64 -d data.txt`
- Passphrase: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

Bandit 11: rot13 with tr

- `cat data.txt | tr A-Za-z N-ZA-Mn-za-m`
- Passphrase: JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

Bandit 12: Lots of decompression

- Copy `data.txt` to `/tmp/tempfolder, xxd -r` to revert hexdump
- Repeating `file -> mv to change file extension -> decompress` until unarchived
- `tar -xf [file]`, `gzip -d [file]`, `bzip2 -d [file]`
- `rm -rf /tmp/tempfolder` to clean up
- Passphrase: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
