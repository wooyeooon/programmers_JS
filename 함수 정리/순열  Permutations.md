- 알고리즘: 주어진 n엘리먼트들의 모든 경우의 수를 계산하는 방법 / O(n!) 시간 복잡도
- 백트래킹 / DFS 활용하여 문제 접근

```javascript
function permutate(arr) {
  const result = [];

  // DFS
  const dfs = (i, arr) => {
    // base condition
    if (i === arr.length) {
      return result.push([...arr]);
    }

    for (let j = i; j < arr.length; j++) {
      // swap
      [arr[i], arr[j]] = [arr[j], arr[i]];
      // DFS
      dfs(i + 1, arr);
      // swap back
      [arr[i], arr[j]] = [arr[j], arr[i]];
    }
  };
  dfs(0, arr);
  return result;
}

console.log(permutate(["a", "b", "c"])); // [a,b,c],[a,c,b],[b,a,c]...
```
