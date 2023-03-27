## Problem : Intersection of Two Arrays-2
[Question Link](https://leetcode.com/problems/intersection-of-two-arrays-ii/description/)

## Complexity
-   Time complexity: *O(NlogN)*
-   Space complexity: *O(N)*

## Solution : (Solved by me)

```cpp
class Solution {
public:
    vector<int> intersect(vector<int>& nums1, vector<int>& nums2) {
        sort(nums1.begin(), nums1.end());
        sort(nums2.begin(), nums2.end());

        int n = nums1.size();
        int m = nums2.size();

        vector<int> res;
        int i = 0, j = 0;

        while(i < n && j < m){
            if(nums1[i] > nums2[j]) j++;
            else if(nums1[i] < nums2[j]) i++;
            else {
                res.push_back(nums1[i]);
                i++;
                j++;
            }
        }

        return res;

    }

};
```


### Resources for better understanding :

[Link 1](https://www.example.com)
[Link 2](https://www.example.com)
[Link 3](https://www.example.com)



