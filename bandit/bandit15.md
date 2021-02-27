# Level 15: Submit Password on Localhost
## Goal
Submitting the password of the current level to port 30000 on localhost.
https://overthewire.org/wargames/bandit/bandit15.html
## Solution
```ssh -i sshkey.private bandit14@localhost
    # sshkey.private contained private ssh key
    # All users on same machine, use localhost
cat /etc/bandit_pass/bandit14
```
etc...
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e