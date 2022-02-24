## Two Strings | Hackerrank

Given two strings, determine if they share a common substring. A substring may be as small as one character.

**Example**
_s1 = "and"_
_s2 = "art"_
These share the common substring _a_.

_s1 = "be"_
_s2 = "cat"_
These do not share a substring.

**Function Description**
Complete the function  _twoStrings_  in the editor below.

twoStrings has the following parameter(s):

-   _string s1:_  a string
-   _string s2:_  another string

**Returns**
-   _string:_  either  `YES`  or  `NO`

**Input Format**

The first line contains a single integer  _p_, the number of test cases.

The following _p_ pairs of lines are as follows:

-   The first line contains string  _s1_.
-   The second line contains string  _s2_.

**Output Format**

For each pair of strings, return  `YES`  or  `NO`.

**Sample Input**
```
2
hello
world
hi
world
```

**Sample Output**
```
YES
NO
```


**Explanation**

We have _p=2_ pairs to check:

1.  _s1="hello",  s2="world"_. The substrings  _"o"_ and  _"l"_ are common to both strings.
2.  _a="hi",  b="world"_.  _s1_ and _s2_ share no common substrings.

**First:**
```javascript
'use strict';

const fs = require('fs');

process.stdin.resume();
process.stdin.setEncoding('utf-8');

let inputString = '';
let currentLine = 0;

process.stdin.on('data', function(inputStdin) {
    inputString += inputStdin;
});

process.stdin.on('end', function() {
    inputString = inputString.split('\n');

    main();
});

function readLine() {
    return inputString[currentLine++];
}

/*
 * Complete the 'twoStrings' function below.
 *
 * The function is expected to return a STRING.
 * The function accepts following parameters:
 *  1. STRING s1
 *  2. STRING s2
 */

function twoStrings(s1, s2) {
  let max_length = Math.max(s1.length, s2.length)
  let isBigger; let isSmaller;
  if(max_length === s1.length) {
    isBigger = s1;
    isSmaller = s2;
    } else {
      isBigger = s2;
      isSmaller = s1;
    } 
  for(let i = 0; i < max_length; i++){
    if(isBigger.includes(isSmaller[i]))
      return "YES"
  } return "NO"
}

function main() {
    const ws = fs.createWriteStream(process.env.OUTPUT_PATH);

    const q = parseInt(readLine().trim(), 10);

    for (let qItr = 0; qItr < q; qItr++) {
        const s1 = readLine();

        const s2 = readLine();

        const result = twoStrings(s1, s2);

        ws.write(result + '\n');
    }

    ws.end();
}

```
