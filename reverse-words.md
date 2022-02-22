## Description
Complete the function that accepts a string parameter, and reverses each word in the string. All spaces in the string should be retained.

Example: 
"This is an example!" ==> "sihT si na !elpmaxe"
"double  spaces"      ==> "elbuod  secaps"

**First:**

```javascript
function reverseWords(str) {
  str = str.split('').reverse().join('').split(' ').reverse().join(' ');
  return str
}
```

