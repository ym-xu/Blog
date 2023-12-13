---
Category:
  - BinarySearch
Diff: Medium
tags:
  - BinarySearch
  - Medium
Update Date: 2023-12-12
share: "true"
---

![[Pasted image 20231212094312.png|Pasted image 20231212094312.png]]
## Note

### Method 1: BinarySearch

#### Code
```python
def searchInSortedMatrix(matrix, target):
    # Write your code here.
    row = 0
    col = len(matrix[0]) - 1

    while row < len(matrix) and col >= 0:
        if matrix[row][col] > target:
            col -= 1
        elif matrix[row][col] < target:
            row += 1
        else:
            return [row, col]
    return [-1, -1]
```
#### Analysis
##### Time Complexity: $O()$
##### Space Complexity: $O()$

