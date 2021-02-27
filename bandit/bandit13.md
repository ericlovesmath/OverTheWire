# Level 13: Hexdump and Zips
## Goal
data.txt is a repeated compressed hexdump.
Suggestion: Make a directory under /tmp and cp the data
## Solution
```cp data.txt /tmp/data/data.txt
cd /tmp/data
xxd -r data.txt extracted
    # Un-hexdumps
file extracted
    # extracted: gzip compressed data, was "data2.bin"
mv extracted extracted.gz
    # gzip -d extracted.gz
    # bzip2 -d extracted.bz2
    # tar -xf extracted.tar
```
etc...
8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL