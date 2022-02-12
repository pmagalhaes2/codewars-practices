## Description
Complete the method/function so that it converts dash/underscore delimited words into camel casing. The first word within the output should be capitalized  **only**  if the original word was capitalized (known as Upper Camel Case, also often referred to as Pascal case).

Example: 
`"the-stealth-warrior"` gets converted to `"theStealthWarrior"`  
`"The_Stealth_Warrior"` gets converted to `"TheStealthWarrior"`

**First:**

```javascript
function  toCamelCase(str) {
	if (str  ==  "") {
		return  "";
	}
	for (let  i  =  0; i  <  str.length; i++) {
		if (str[i] ==  "_"  ||  str[i] ==  "-") {
			i++;
			let  capitalized  =  str[i].toUpperCase();
			str  =  str.replace(str[i], capitalized);
		}
	}
	str  =  str.replace(/(-|_)/g, "");
	return  str;
}
```