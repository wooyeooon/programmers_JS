```javascript
const stringA = "listen";
const stringB = "silent";

// #1 split(), sort(), and join()
function isAnagram(strA, strB) {
	if(strA.length !== strB.length) {
		return false;
	}
	return strA.Split("").sort().join() === strB.Split("").sort().join()
}

console.log(isAnagram(stringA, stringB)); // true

// #2 map = {}
function isAnagram(strA, strB) {
	if (strA.length !== strB.length) {
		return false;
}
const hashMap = {};
for (const char of strA) {
 // {l:1, i:1, s:1}
	hashMap[char] = hashMap[char] ? hashMap[char] + 1 : 1;
}

for (const char pf strB) {
	if (!hashMap[char]) {
		return false;
	}
	hashMap[char]--;
	}
	return true;
}

console.log(isAnagram(stringA, stringB)); // true
```
