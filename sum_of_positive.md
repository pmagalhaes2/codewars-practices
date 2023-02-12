## Description
You get an array of numbers, return the sum of all of the positives ones.

Example:

`[1,-4,7,12]`  => `1 + 7 + 12 = 20`  

Note: if there is nothing to sum, the sum is default to `0`.

**First:**

```javascript
function positiveSum(arr) {
  if (arr.length === 0) return 0;

  const arrayFiltrado = arr.filter((num) => num > 0);

  return arrayFiltrado.length === 0
    ? 0
    : arrayFiltrado.reduce((accum, curr) => accum + curr);
}

```

**Second:**

```javascript
function positiveSum(arr) {
  const arrayFiltrado = arr.filter((num) => num > 0);

  return arr.length === 0 || arrayFiltrado.length === 0
    ? 0
    : arrayFiltrado.reduce((accum, curr) => accum + curr);
}
```

**Third:**

```javascript 
function positiveSum(arr) {
  return arr.filter((num) => num > 0).reduce((accum, curr) => accum + curr, 0);
}
```

