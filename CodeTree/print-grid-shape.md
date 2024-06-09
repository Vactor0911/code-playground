# 격자 모양 출력하기
> 쉬움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [격자 모양 출력하기](https://www.codetree.ai/missions/4/problems/print-grid-shape/description "격자 모양 출력하기")

</br>

n x n 크기의 격자의 칸 위에 m 개의 점이 놓여져 있습니다.

각 점의 크기는 해당 칸의 행 번호와 열 번호의 곱이 됩니다.

각 점의 위치에 해당하는 정보가 주어질 때, 격자의 모양을 출력하는 프로그램을 작성해보세요.

단, 행과 열의 번호는 1부터 시작됩니다.

</br>

## 입력 형식
첫 번째 줄에 격자의 크기 n과 점의 개수 m이 공백을 두고 주어집니다.

두 번째 줄부터 m개의 줄에 걸쳐 각 점의 행 번호와 열 번호가 공백을 사이에 두고 주어집니다.

주어진 m개의 점의 위치는 모두 다름을 가정해도 좋습니다.

- 1 ≤ n ≤ 10

- 1 ≤ m ≤ n * n

</br>

## 출력 형식
첫 번째 줄부터 n개의 줄에 걸쳐, 각 행에 해당하는 n개의 값을 공백을 사이에 두고 출력합니다.

점이 있는 칸은 점의 크기를, 나머지 칸은 0을 출력합합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
n, m = tuple(map(int, input().split()))
array = [
    [0 for _ in range(n)]
    for _ in range(n)
]

for i in range(m):
    r, c = tuple(map(int, input().split()))
    array[r-1][c-1] = r * c

for row in array:
    for element in row:
        print(element, end=" ")
    print()
```

</div>
</details>