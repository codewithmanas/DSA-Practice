## Problem : Reverse words in a given string
[Question Link](https://practice.geeksforgeeks.org/problems/reverse-words-in-a-given-string5459/1)

## Solution : (Solved by me)

```cpp
//{ Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

// } Driver Code Ends

class Solution
{
    public:
    //Function to reverse words in a given string.
    string reverseWords(string S) 
    { 
        // code here 
        int size = S.size();
        // int count = 0;
        string res, temp;
        for(int i = size-1; i >= 0; i--){
            if(S[i] == '.'){
                reverse(temp.begin(), temp.end());
                res.append(temp);
                res.append(".");
                temp.clear();
            }else{
                temp.push_back(S[i]);
            }
        }
        if(temp != ""){
            reverse(temp.begin(), temp.end());
            res.append(temp);
            temp.clear();
        }
        return res;
    } 
};

//{ Driver Code Starts.
int main() 
{
    int t;
    cin >> t;
    while (t--) 
    {
        string s;
        cin >> s;
        Solution obj;
        cout<<obj.reverseWords(s)<<endl;
    }
}
// } Driver Code Ends
```


### Resources for better understanding :

[Append a char to the end of a string in C++](https://www.techiedelight.com/append-char-end-string-cpp/)
[String Concatenation in C++: 4 Ways To Concatenate Strings](https://www.digitalocean.com/community/tutorials/string-concatenation-in-c-plus-plus)
[Different Methods to Reverse a String in C++](https://www.geeksforgeeks.org/reverse-a-string-in-c-cpp-different-methods/)
[std::string::clear in C++](https://www.geeksforgeeks.org/stdstringclear-in-cpp/)



