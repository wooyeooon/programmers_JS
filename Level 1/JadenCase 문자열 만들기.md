# JadenCase 문자열 만들기

[문제 바로가기](https://school.programmers.co.kr/learn/courses/30/lessons/12951)

**문제설명**

> JadenCase란 모든 단어의 첫 문자가 대문자이고, 그 외의 알파벳은 소문자인 문자열입니다. 단, 첫 문자가 알파벳이 아닐 때에는 이어지는 알파벳은 소문자로 쓰면 됩니다. (첫 번째 입출력 예 참고)
> 문자열 s가 주어졌을 때, s를 JadenCase로 바꾼 문자열을 리턴하는 함수, solution을 완성해주세요.

**입출력 예**
| s | return |
| --- | --- |
| "3people unFollowed me" | "\*\*\"3people Unfollowed Me" |
| "for the last week" | "For The Last Week" |

---

**나의 풀이**

```javascript
function solution(s) {
  var words = s.split(" ");
  return words
    .map(
      (word) => word.charAt(0).toUpperCase() + word.substring(1).toLowerCase()
    )
    .join(" ");
}
```

**참고 풀이**

```javascript
function solution(s) {
  var answer = "";
  for (let i = 0; i < s.length; i++) {
    if (i === 0 || s[i - 1] === " ") {
      answer += s[i].toUpperCase();
    } else {
      answer += s[i].toLowerCase();
    }
  }
  return answer;
}
```
