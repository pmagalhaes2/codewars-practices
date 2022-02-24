
## Description

The first century spans from the **year 1** up to _and including_ the year 100, the second century - from the year 101 up to _and including_ the year 200, etc.

Given a year, return the century it is in.

**Examples:**
```text
1705 --> 18
1900 --> 19
1601 --> 17
2000 --> 20
```

**First:**
```javascript
function century(year) {
  return Math.ceil(year / 100)
}
```

**Second:**
```javascript
function century(year) {
  if (year % 100 > 0) {
    return Math.ceil(year / 100);
  }
  return year / 100;
}
```
