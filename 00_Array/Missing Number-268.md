## Problem : Missing Number-268

[Question Link](https://leetcode.com/problems/missing-number/description/)

## Complexity
-   Time complexity:
-   Space complexity:

## Solution : (Solved by me)

```cpp
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int sum = 0;
        for(int num : nums){
            sum += num;
        }
        int expect = (nums.size()) * (nums.size() + 1) / 2;
        return expect - sum;
    }
};
```

## Solution : 2

```cpp
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        sort(nums.begin(), nums.end());
        int i = 0;
        for(; i < nums.size(); i++){
            if(nums[i] != i)
                return i;
        }
        return i;
    }
};
```


### Resources for better understanding :