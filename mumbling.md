## Description
This time no story, no theory. The examples below show you how to write function `accum` :

**Examples:**
```text
accum("abcd") -> "A-Bb-Ccc-Dddd"
accum("RqaEzty") -> "R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy"
accum("cwAt") -> "C-Ww-Aaa-Tttt"
```

The parameter of accum is a string which includes only letters from `a..z` and `A..Z`

**First:**

```javascript
function accum(s) {
  let newStr = "";
  for (let i = 0; i < s.length; i++) {
    const hasUpper = (str) => /[A-Z]/.test(str);

    if (s[i].hasUpper) {
      newStr += s[i].toLowerCase() + s[i].repeat(i) + "-";
    } else {
      newStr += s[i].toUpperCase() + s[i].toLowerCase().repeat(i) + "-";
    }
  }
  return newStr.substring(0, newStr.length - 1);
}

```

