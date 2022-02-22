## Description
Welcome.

In this kata you are required to, given a string, replace every letter with its position in the alphabet.

If anything in the text isn't a letter, ignore it and don't return it.

"a" = 1, "b" = 2, etc.

Example:
```text 
alphabetPosition("The sunset sets at twelve o' clock.")
```

Should return
**"20 8 5 19 21 14 19 5 20 19 5 20 19 1 20 20 23 5 12 22 5 15 3 12 15 3 11"** (as a string)


**First:**

```javascript
function alphabetPosition(text) {
    var alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    text = text.normalize("NFD").replace(/([\u0300-\u036f]|[^0-9a-zA-Z])/g, "");
    var code = [];
    for (var i in text) {
        code.push(alphabet.indexOf(text[i].toUpperCase()) + 1);
    }
    return code.join(' ');
}
```

