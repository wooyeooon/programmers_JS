#**ad 제거하기**
[문제 바로가기](https://school.programmers.co.kr/learn/courses/30/lessons/181870)

**문제설명**

> 문자열 배열 strArr가 주어집니다. 배열 내의 문자열 중 "ad"라는 부분 문자열을 포함하고 있는 모든 문자열을 제거하고 남은 문자열을 순서를 유지하여 배열로 return 하는 solution 함수를 완성해 주세요.

**입출력 예**
| strArr | result |
| --- | --- |
| ["and","notad","abcd"] | ["and","abcd"] |
| ["there","are","no","a","ds"] | ["there","are","no","a","ds"] |

---

**나의 풀이**

```javascript
function solution(strArr) {
  return strArr.filter((el) => !el.includes("ad"));
}
```
