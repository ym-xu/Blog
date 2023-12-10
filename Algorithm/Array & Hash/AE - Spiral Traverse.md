---
Category:
  - Array
Diff: Medium
tags:
  - Array
  - Medium
Update Date: 2023-12-10
share: "true"
---

![[Pasted image 20231210155721.png|Pasted image 20231210155721.png]]
## Note

### Method 1
Advancement of [[59. Spiral Matrix II|59. Spiral Matrix II]]
#### Code
```python 
def spiralTraverse(array):
    # Write your code here.
    res = []
    startRow, endRow = 0, len(array) - 1
    startCol, endCol = 0, len(array[0]) - 1

    while startRow <= endRow and startCol <= endCol:
        print(startRow, endRow, startCol, endCol)
        for col in range(startCol, endCol + 1):
            res.append(array[startRow][col])

        for row in range(startRow + 1, endRow + 1):
            res.append(array[row][endCol])

        for col in reversed(range(startCol, endCol)):
            if startRow == endRow:
                break
            res.append(array[endRow][col])

        for row in reversed(range(startRow + 1, endRow)):
            if startCol == endCol:
                break
            res.append(array[row][startRow])

        startRow += 1
        endRow -= 1
        startCol += 1
        endCol -= 1

    return res

```
#### Analysis
##### Time Complexity: $O(n)$
##### Space Complexity: $O(n * n)$

