## Problem : Move Zeroes-283
[Question Link](https://leetcode.com/problems/move-zeroes/description/)

## Complexity
-   Time complexity: O(n)
-   Space complexity: O(1)

## Solution : (Solved by me)

```cpp
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int size = nums.size();
        if(size < 2) return;
        int index = 0;
        int count = 0;

        for(int i = 0; i < size; i++){
            if(nums[i] == 0){
                count++;
            }else {
                nums[index] = nums[i];
                index++;
            }
        }

        if(count == 0 || index == 0){
            return;
        }

        index = size - 1;
        while(count--){
            nums[index] = 0;
            index--;
        }
    }
};
```

## Best-Solution :

```cpp
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int index = 0;
        for(int i = 0; i < nums.size(); i++){
            if(nums[i] != 0){
                swap(nums[i], nums[index]);
                index++;
            }
        }
    }
};
```


### Resources for better understanding :