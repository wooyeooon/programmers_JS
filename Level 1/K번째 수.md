# k번째 수

[문제 바로가기](https://school.programmers.co.kr/learn/courses/30/lessons/42748)

**문제설명**

> 배열 array의 i번째 숫자부터 j번째 숫자까지 자르고 정렬했을 때, k번째에 있는 수를 구하려 합니다.
> 예를 들어 array가 [1, 5, 2, 6, 3, 7, 4], i = 2, j = 5, k = 3이라면
> array의 2번째부터 5번째까지 자르면 [5, 2, 6, 3]입니다.
> 1에서 나온 배열을 정렬하면 [2, 3, 5, 6]입니다.
> 2에서 나온 배열의 3번째 숫자는 5입니다.
> 배열 array, [i, j, k]를 원소로 가진 2차원 배열 commands가 매개변수로 주어질 때, commands의 모든 원소에 대해 앞서 설명한 연산을 적용했을 때 나온 결과를 배열에 담아 return 하도록 solution 함수를 작성해주세요.

**입출력 예**
| array | commands | return
| --- | ----- | --- |
| [1, 5, 2, 6, 3, 7, 4] | [[2, 5, 3], [4, 4, 1], [1, 7, 3]] | [5, 6, 3]

---

**나의 풀이**

```javascript
function solution(array, commands) {
  let answer = []; //빈 배열 설정

  for (let i = 0; i < commands.length; i++) {
    let start = commands[i][0]; //시작 값 지정
    let end = commands[i][1]; //종료 값 지정
    let k = commands[i][2]; //출력 값 지정

    let newArr = array.slice(start - 1, end); //범위 내의 값을 복사하여 새로운 배열에 저장

    newArr.sort((a, b) => a - b); //배열 정렬
    answer.push(newArr[k - 1]); //특정 값을 빈 배열에 넣는다.
  }
  return answer;
}
```

**참고 풀이**

```javascript
function solution(array, commands) {
  return commands.map((v) => {
    return array
      .slice(v[0] - 1, v[1])
      .sort((a, b) => a - b)
      .slice(v[2] - 1, v[2])[0];
  });
}
```
