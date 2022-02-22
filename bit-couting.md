## Description
Write a function that takes an integer as input, and returns the number of bits that are equal to one in the binary representation of that number. You can guarantee that input is non-negative.

Example: The binary representation of **1234** is **10011010010**, so the function should return **5** in this case

**First:**

```javascript
var countBits = function(n) {
  if(n === 0) return 0;
  if(n < 0 || n === null) return false;
  return n.toString(2).match(/1/g).length;
};
```
**Second:**
```javascript
var countBits = function (n) {
  n = n.toString(2);
  let cont = 0;
  for (let el of n) {
    if (el == 1) cont++;
  }
  return cont;
};
```