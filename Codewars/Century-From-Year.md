## Problem : Century From Year
[Question Link](https://www.codewars.com/kata/5a3fe3dde1ce0e8ed6000097)

## Statement : 
#### Introduction
The first century spans from the year 1 up to and including the year 100, the second century - from the year 101 up to and including the year 200, etc.

#### Task
Given a year, return the century it is in.

#### Examples 
```sh
    1705 --> 18
    1900 --> 19
    1601 --> 17
    2000 --> 20
```

Note: this kata uses strict construction as shown in the description and the examples, you can read more about it [here](https://en.wikipedia.org/wiki/Century)

**Tags:** : `Mathematics`, `Fundamentals`

## Complexity
-   Time complexity:
-   Space complexity:

## Solution : (Solved by me)

```javascript
function century(year) {
  let number = year/100;
  return Math.ceil(number);
}
```


### Resources for better understanding :

[Link 1](https://www.example.com)
[Link 2](https://www.example.com)
[Link 3](https://www.example.com)



