# 01-jan-2021

### 1 - leetcode remove-duplicates-from-sorted-array


- Algorithm
  - two pointers, slow i and fastrunner j
  - increment j tot skip duplicates
  - when nums[j] != nums[i], duplicate run has come to an end, thus copy value 
  - Repeat the same process untill j reaches end of the array


```
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        

        if len(nums) == 0:
            return 0
        
        i = 0
        for j in range(1, len(nums)):
            if nums[j] != nums[i]:
                i += 1
                nums[i] = nums[j]
                
        return i+1


```
