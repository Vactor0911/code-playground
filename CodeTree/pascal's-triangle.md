# 파스칼의 삼각형
> 보통

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [파스칼의 삼각형](https://www.codetree.ai/missions/4/problems/pascal's-triangle/description "파스칼의 삼각형")

</br>

행의 크기가 정수 n으로 주어집니다. 행의 크기가 n인 파스칼 삼각형을 출력하는 프로그램을 작성해보세요. 파스칼 삼각형이란 다음과 같은 형태로 나타나며, (i, j)에 적힌 숫자가 (i - 1, j - 1)에 적힌 숫자와 (i - 1, j)에 적힌 숫자의 합으로 나타납니다.

n = 5일때의 예

| | | | | |
|:--:|:--:|:--:|:--:|:--:|
|1| | | | |
|1|1| | | |
|1|2|1| | |
|1|3|3|1| |
|1|4|6|4|1|

</br>

## 입력 형식
첫 번째 줄에 n이 주어집니다.

- 1 ≤ n ≤ 15

</br>

## 출력 형식
행의 크기가 n인 파스칼의 삼각형을 입출력 예제와 같이 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
size = int(input())
array = [
    [1 for _ in range(i+1)]
    for i in range(size)
]

for i in range(2, size):
    for j in range(1,i):
        array[i][j] = array[i-1][j-1] + array[i-1][j]

for row in array:
    for element in row:
        print(element, end=" ")
    print()
```

</div>
</details>