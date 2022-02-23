## Description

Define a function that takes one integer argument and returns logical value  `true`  or  `false`  depending on if the integer is a prime.

Per Wikipedia, a prime number (or a prime) is a natural number greater than 1 that has no positive divisors other than 1 and itself.

## Requirements

-   You can assume you will be given an integer input.
-   You can not assume that the integer will be only positive. You may be given negative numbers as well (or  `0`).
-   **NOTE on performance**: There are no fancy optimizations required, but still  _the_  most trivial solutions might time out. Numbers go up to 2^31 (or similar, depends on language version). Looping all the way up to  `n`, or  `n/2`, will be too slow.
  
 
**Example:**
```text
is_prime(1)  /* false */
is_prime(2)  /* true  */
is_prime(-1) /* false */
```

**First:**
```javascript
function isPrime(num) {
  if (num <= 1 || (num % 2 == 0 && num != 2)) return false;
  let limit = Math.sqrt(num);
  let divisores = 1;
  for (let i = 1; i <= limit; i++) {
    if (num % i === 0) {
      divisores++;
    }
  }
  return divisores == 2;
}
```

**Time-out error solutions:**
```javascript
//First
function isPrime(num) {
  if (num <= 1) return false;
  for (let divisor = 2; divisor < num; divisor++)
    if (num % divisor == 0) return false;
  return true;
}

//Second
function isPrime(num) {
  let divisores = 0;
  for (var count = 1; count <= num; count++) if (num % count == 0) divisores++;

  if (divisores == 2) return true;
  return false;
}

//Third
function isPrime(num) {
  let divisores = 0;
  let count = 0;
  while (count <= num) {
    count++;
    if (num % count == 0) divisores++;
  }
  if (divisores == 2) return true;
  return false;
}

//Fourth
function isPrime(num) {
  let divisores = 0;
  for (var count = 1; count <= num; count++) {
    if (divisores > 2) return false;
    if (num % count == 0) divisores++;
  }
  if (divisores == 2) return true;
  return false;
}
```
