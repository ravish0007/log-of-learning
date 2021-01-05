# 05-jan-2021

### 1 - AGILE


Individuals and interactions over processes and tools
Working software over comprehensive documentation
Customer collaboration over contract negotiation
Responding to change over following a plan


### 2 - binary search tree vertical lines



```python

class Solution:
    def solve(self, root):
        left = right = 0

        def dfs(root, x):
            nonlocal left, right
            if not root:
                return
            left = min(x, left)
            right = max(x, right)
            dfs(root.left, x - 1)
            dfs(root.right, x + 1)

        dfs(root, 0)
        return right - left + 1

```
