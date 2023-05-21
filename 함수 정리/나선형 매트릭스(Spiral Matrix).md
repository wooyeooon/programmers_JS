- 2D Array / 2차원 배열 순회 문제
- M x N 사이즈의 매트릭스의 엘레멘트를 나선형 모양으로 순회

문제 접근 방법

- 4곳의 코너 포인터를 각각 변수에 저장 초기화
- Top Left 코너에서 시작, 첫번째 row 왼쪽 → 오른쪽으로 순회. 순회가 끝나면 Top포인터 +1 증가
- Right Top 코너에서 시작, 맨 우측 위 → 아래로 순회. 순회가 끝나면 Right 포인터 -1 감소
- Right Bottom 코너에서 시작 맨우츨 오른쪽 → 왼쪽으로 순회. 순회 후 Bottom 포인터 -1 감소
- Left 포인터에서 시작, 왼쪽 → 오른쪽으로 순회 Left포인터 +1

```javascript
function spiralMatrix(matrix) {
	const result = []

	let left = 0;
	let right = matrix[0].length -1;
	let top = 0;
	let bottom = matrix.length -1;

	while (left <= right && top <= bottom) {

		for (let i = left; i <= right; i++) {
			result.push(matrix[top][i])
		}
		top++;

		for (let i = top; i <= bottom; i++) {
			result.push(matrix[i][right])
		}
		right--;

		if (top <= bottom) {
			for (let i = right; i>= left; i--) {
				result.push(matrix[bottom][i])
			}
			bottom--;
		}

		if (left <= right) {
			for(let i = bottom; i >= top; i-- {
				result.push(matrix[i][left])
			}
			left++;
		}

	}
	return result;
}

const test1 = [[1, 2, 3], [4, 5, 6], [7, 8, 9]] // [1,2,3,6,9,8,7,4,5]
const test2 = [[1,2,3,4], [5, 6, 7, 8], [9, 10, 11, 12]]// [1,2,3,4,8,12,11,10,9,5,6,7]
```
