---
Category:
  - Array
Diff: Hard
tags:
  - Array
  - Hard
Update Date: 2024-01-14
share: "true"
---

![[Pasted image 20240114194551.png|Pasted image 20240114194551.png]]
## Note

### Method 1

#### Code
```python
def apartmentHunting(blocks, reqs):
    # create an array to store all the maxdistance
    # traverse allover the blocks
        # traverse every reqs
            # traverse all blocks
                # find the min distance
            # get the max dis
    # return res 

    mindis = [float('-inf') for i in blocks]
    res = 0
    final_minidx = float('inf')

    for i in range(len(blocks)):
        for req in reqs:
            closest_dis = float('inf')
            for j in range(len(blocks)):
                if blocks[j][req]:
                    closest_dis = min(closest_dis, abs(i - j))
            mindis[i] = max(mindis[i], closest_dis)
        if mindis[i] < final_minidx:
            final_minidx = mindis[i]
            res = i
    return res
```
#### Analysis
##### Time Complexity: $O(n^2)$
##### Space Complexity: $O(n)$

