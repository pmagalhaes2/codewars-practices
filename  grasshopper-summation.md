
## Sumation

Write a program that finds the summation of every number from 1 to num. The number will always be a positive integer greater than 0.

 
**For example:**
```text
summation(2) -> 3
1 + 2

summation(8) -> 36
1 + 2 + 3 + 4 + 5 + 6 + 7 + 8
```


**First:**
```javascript
var summation = function (num) {
  let sum = 0;
  for(let i = num; i > 0; i--) {
    sum += i
  }
  return sum;
}
```

**Second:**
```javascript
var summation = function (num) {
  let i = 0, sum = 0;
  while(i <= num) {
    sum += i
    i++
  }
  return sum;
}
```