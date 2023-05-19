# 문자열 뒤의 n글자

[문제 바로가기](https://school.programmers.co.kr/learn/courses/30/lessons/181910)

**문제설명**

> 문자열 my_string과 정수 n이 매개변수로 주어질 때, my_string의 뒤의 n글자로 이루어진 문자열을 return 하는 solution 함수를 작성해 주세요.

**입출력 예**
| my_string | n | result
| --- | --- | --- |
| "ProgrammerS123" | 11 | "grammerS123"
| "He110W0r1d" | 5 | "W0r1d"

---

**나의 풀이**

```javascript
function solution(my_string, n) {
  return my_string.slice(-n);
}
```
