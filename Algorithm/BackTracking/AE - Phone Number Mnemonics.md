---
Category:
  - BackTracking
Diff: Medium
tags:
  - BackTracking
  - Medium
Update Date: 2023-12-27
share: "true"
---

![[Pasted image 20231227094807.png|Pasted image 20231227094807.png]]
## Note

### Method 1
Variation of the [[17. Letter Combinations of a Phone Number|17. Letter Combinations of a Phone Number]]
#### Code
```python
def phoneNumberMnemonics(phoneNumber):
    # Write your code here.
    letters = {
        "0": "0",
        "1": "1",
        "2": "abc",
        "3": "def",
        "4": "ghi",
        "5": "jkl",
        "6": "mno",
        "7": "pqrs",
        "8": "tuv",
        "9": "wxyz",
    }
    res = []
    path = []
    backtracking(phoneNumber, letters, 0, res, path)
    return res

def backtracking(phoneNumber, letters, startidx, res, path):
    if len(path) == len(phoneNumber):
        res.append(''.join(path))
        return

    currletter = phoneNumber[startidx]

    for i in letters[currletter]:
        path.append(i)

        backtracking(phoneNumber, letters, startidx + 1, res, path)

        path.pop()
```
#### Analysis
##### Time Complexity: $O()$
##### Space Complexity: $O()$

