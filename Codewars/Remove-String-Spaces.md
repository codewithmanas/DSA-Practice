## Problem : Remove String Spaces
[Question Link](https://www.codewars.com/kata/57eae20f5500ad98e50002c5)

## Statement : Write a function that removes the spaces from the string, then return the resultant string.
```sh
    Input -> Output
    "8 j 8   mBliB8g  imjB8B8  jl  B" -> "8j8mBliB8gimjB8B8jlB"
    "8 8 Bi fk8h B 8 BB8B B B  B888 c hl8 BhB fd" -> "88Bifk8hB8BB8BBBB888chl8BhBfd"
    "8aaaaa dddd r     " -> "8aaaaaddddr"
```

**Tags:** : `Strings`, `Fundamentals`

## Complexity
-   Time complexity:
-   Space complexity:

## Solution : (Solved by me)

```javascript
function noSpace(x){
  let arr = x.split(" ");
  let str = arr.join("");
  return str;
}
```


### Resources for better understanding :

[Link 1](https://www.example.com)
[Link 2](https://www.example.com)
[Link 3](https://www.example.com)



