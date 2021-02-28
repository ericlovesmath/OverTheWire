# Level 12: Rotating Letters
## Goal
All (a-z) and (A-Z) are rotated by 13 letters
## Solution
```
cat data.txt | tr [a-z][A-Z] [n-za-m][N-ZA-M]
    # tr translates first to second
    # mapping function
    # Brackets not needed
```
5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu