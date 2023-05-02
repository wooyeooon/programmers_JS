#**x만큼 간격이 있는 n개의 숫자**
[문제 바로가기](https://school.programmers.co.kr/learn/courses/30/lessons/12954)

**문제설명**

> 함수 solution은 정수 x와 자연수 n을 입력 받아, x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴해야 합니다.
> 다음 제한 조건을 보고, 조건을 만족하는 함수, solution을 완성해주세요.

**입출력 예**
| n | x | answer |
| --- | --- | --- | --- |
| 2 | 5 | [2, 4, 6, 8, 10] |
| 4 | 3 | [4, 8, 12] |
| -4 | 2 | [-4, -8] |

---

**나의 풀이**

```javascript
function solution(x, n) {
  var answer = [];
  for (i = 0; i < n; i++) {
    answer[i] = x * (i + 1);
  }
  return answer;
}
```

**참고풀이**

```javascript
function solution(x, n) {
  return Array(n)
    .fill(x)
    .map((v, i) => (i + 1) * v);
}
```
