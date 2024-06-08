# 격자로 사각형 만들기
> --

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [격자로 사각형 만들기](https://www.codetree.ai/missions/4/problems/print-grid-in-rectangle/description "격자로 사각형 만들기")

</br>

아래 조건을 만족하도록 격자를 만들어 출력하는 프로그램을 작성해보세요.

- 첫 번째 행과 첫 번째 열에는 모두 1이 들어갑니다.

- 나머지 칸들은 바로 위의 값과 바로 왼쪽 값, 그리고 왼쪽 위의 값의 합이 되어야 합니다.

- 크기는 n x n 입니다.

</br>

## 입력 형식
첫 번째 줄에 정수 n이 주어집니다.

- 2 ≤ n ≤ 10

</br>

## 출력 형식
첫 번째 줄부터 n개의 줄에 걸쳐, 각 행에 해당하는 n개의 수를 공백을 사이에 두고 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
size = int(input())
array = [
    [1 for _ in range(size)]
    for _ in range(size)
]

for i in range(1, size):
    for j in range(1, size):
        array[i][j] = array[i-1][j] + array[i][j-1] + array[i-1][j-1]

for row in array:
    for element in row:
        print(element, end=" ")
    print()
```

</div>
</details>