## Problem : Subarray with given sum

[Question Link](https://practice.geeksforgeeks.org/problems/subarray-with-given-sum-1587115621/1)

## Complexity
-   Time complexity: _O(N)_
-   Space complexity: _O(1)_

## Solution : (Solved by me)

```cpp
///{ Driver Code Starts
#include <bits/stdc++.h>
using namespace std;


// } Driver Code Ends
class Solution
{
    public:
    //Function to find a continuous sub-array which adds up to a given number.
    vector<int> subarraySum(vector<int>arr, int n, long long s)
    {
        int l = 0;
        int r = 0;
        vector<int> res;
        bool flag = false;
        int sum = arr[0];
        
        if(s == 0) {
            res.push_back(-1);
            return res;
        }
        while(r < n) {
            if( sum == s) {
                flag = true;
                break;
            }
            else if(sum < s) {
                r++;
                sum += arr[r];
            }else {
                sum -= arr[l];
                l++;
            }
        }
        
        if(flag) {
            res.push_back(l+1);
            res.push_back(r+1);
            
        }else {
            res.push_back(-1);
        }
        return res;
    }
};

//{ Driver Code Starts.

int main()
 {
    int t;
    cin>>t;
    while(t--)
    {
        int n;
        long long s;
        cin>>n>>s;
        vector<int>arr(n);
        // int arr[n];
        const int mx = 1e9;
        for(int i=0;i<n;i++)
        {
            cin>>arr[i];
        }
        Solution ob;
        vector<int>res;
        res = ob.subarraySum(arr, n, s);
        
        for(int i = 0;i<res.size();i++)
            cout<<res[i]<<" ";
        cout<<endl;
        
    }
	return 0;
}
// } Driver Code Ends
```


### Resources for better understanding :

[Link 1](https://youtu.be/Ofl4KgFhLsM)
[Link 2](https://youtu.be/-Mu95hv8EHw)
[Link 3](https://www.example.com)



