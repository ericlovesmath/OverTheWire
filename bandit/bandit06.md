# Level 6: Finding Files with conditions
## Goal
Read the file in the directory "inhere" that are:
    human-readable
    1033 bytes in size
    not executable
## Solution
```
cd inhere
find . -readable -size 1033c ! -executable`
    # ./maybehere07/.file2
cat ./maybehere07/.file2
```
DXjZPULLxYr17uwoI01bNLQbtFemEgo7