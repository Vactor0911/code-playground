# 격자 반대로 채우기
> --

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [격자 반대로 채우기](https://www.codetree.ai/missions/4/problems/grid-anti-fill/description "격자 반대로 채우기")

</br>

n x n 크기의 격자에 정수를 채워넣으려고 합니다. 1부터 시작해서 차례대로 n² 까지 채워넣는데, 다음 그림과 같이 오른쪽 아래에서 부터 위 아래 지그재그 방향으로 채워넣는 프로그램을 작성해보세요.

| | | | |
|:--:|:--:|:--:|:--:|
|13|12|5|4|
|14|11|6|3|
|15|10|7|2|
|16|9|8|1|

</br>

## 입력 형식
첫 번째 줄에 격자의 크기에 해당하는 정수 n이 주어집니다.

- 1 ≤ n ≤ 10

</br>

## 출력 형식
첫 번째 줄부터 n개의 줄에 걸쳐, 각 행에 해당하는 n개의 숫자를 공백을 사이에 두고 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
size = int(input())
array = [
    [0 for _ in range(size)]
    for _ in range(size)
]

num = 1
for i in range(size-1, -1, -1):
    if (size - i -1) % 2 == 0:
        for j in range(size-1, -1, -1):
            array[j][i] = num
            num += 1
    else:
        for j in range(size):
            array[j][i] = num
            num += 1

for row in array:
    for element in row:
        print(element, end=" ")
    print()
```

</div>
</details>