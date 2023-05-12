#**N의 배수 고르기**
[문제 바로가기](https://school.programmers.co.kr/learn/courses/30/lessons/120905)

**문제설명**

> 정수 n과 정수 배열 numlist가 매개변수로 주어질 때, numlist에서 n의 배수가 아닌 수들을 제거한 배열을 return하도록 solution 함수를 완성해주세요.

**입출력 예**
| n | numlist | result
| --- | --- | --- |
| 3 | [4, 5, 6, 7, 8, 9, 10, 11, 12] | [6, 9, 12] |
| 5 | [1, 9, 3, 10, 13, 5] | [10, 5] |
| 12 | [2, 100, 120, 600, 12, 12] | [120, 600, 12, 12] |

---

**나의 풀이**

```javascript
function solution(n, numlist) {
  return numlist.filter((num) => num % n === 0);
}
```
