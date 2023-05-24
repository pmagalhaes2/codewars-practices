Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).

Examples:

```text
solution('abc', 'bc') // returns true
solution('abc', 'd') // returns false
```

**First:**
```javascript
function solution(str, ending){
  return str.slice(-ending.length) === ending || ending === '';
}
```