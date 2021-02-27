# Level 7: Finding files with more conditions
## Goal
Read the file in the server that are:
    owned by user bandit7
    owned by group bandit6
    33 bytes in size
## Solution
```cd inhere
find / -group bandit6 -user bandit7 -size 33c 2>/dev/null`
    # "/" is the root 
    # "2>/dev/null" routes errors (FD #2) to "/dev/null"
    # Essentially stops all "Permission denied" errors
    # /var/lib/dpkg/info/bandit7.password
cat /var/lib/dpkg/info/bandit7.password
```
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs