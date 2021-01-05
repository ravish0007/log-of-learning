# 04-jan-2021

### 1 - binarysearch Tree top view


- Algorithm
  - bfs cuz dfs ruins
  - operate on depths, should have used dict


```python

class Solution:
    def solve(self, root):
        seen = set()
        eles = []

        q = [(root,0)]

        while q:
            ele, depth = q.pop(0)
            if ele:
                if depth not in seen:
                    seen.add(depth)
                    eles.append((ele.val, depth))
                q.append((ele.left, depth-1))
                q.append((ele.right, depth+1))

        return [ i[0] for i in sorted(eles, key=lambda x:x[1]) ]


```
### 2 - RSA secureid working


- Overview
  - synced clock
  - hash(clock, secret_in_memory)
  - one minute window prevents clock errors



