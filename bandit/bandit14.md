# Level 14: Private SSH Key
## Goal
Password is in /etc/bandit_pass/bandit14
Can only be read by user bandit14
## Solution
```
ssh -i sshkey.private bandit14@localhost
    # sshkey.private contained private ssh key
    # All users on same machine, use localhost
cat /etc/bandit_pass/bandit14
```
etc...
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e