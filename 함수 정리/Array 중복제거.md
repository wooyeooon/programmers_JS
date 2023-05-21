```javascript
// Set()
const nums = [1, 2, 3, 6, 6, 7, 2, 2, 8, 9];

const mySet = new Set();
mySet.add(1);
mySet.add(2);
mySet.add(2);

console.log(mySet); // {1, 2}

const uniqueNums = [...new Set(nums)];
console.log(uniqueNums); // 1, 2, 3, 6, 7, 2, 8, 9
```

```javascript
// indexOf() : 처음 발견한 값의 인덱스만 반환
const nums = [1, 2, 3, 6, 6, 7, 2, 2, 8, 9];

const uniqueNums = nums.filter((item, position) => {
  return nums.indexOf(item) === position;
});

console.log(uniqueNums); // 1, 2, 3, 6, 7, 2, 8, 9

// filter() : 조건에 부합하는 값만 리턴
```

```javascript
// caching / frequency map
const nums = [1, 2, 3, 6, 6, 7, 2, 2, 8, 9];

function uniqueNums(arr) {
  const uniqueElements = {};
  const result = [];
  for (let element of arr) {
    if (!uniqueElements[element]) {
      result.push(element);
    }
    uniqueElements[element] = element;
  }
  return result;
}

console.log(uniqueNums(nums));
```
