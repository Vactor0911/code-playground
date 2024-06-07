# 대각선으로 숫자 채우기
> 어려움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [대각선으로 숫자 채우기](https://www.codetree.ai/missions/4/problems/diagonal-numbering/description "대각선으로 숫자 채우기")

</br>

n * m크기의 직사각형에 숫자를 1부터 순서대로 1씩 증가시키며 왼쪽 위에서부터 시작하여 오른쪽 아래 쪽까지 다음과 같은 방향으로 숫자들을 쭉 채우는 코드를 작성해보세요.

| | | | | | |
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|2|4|7|11|15|
|3|5|8|12|16|19|
|6|9|13|17|20|22|
|10|14|18|21|23|24|

</br>

## 입력 형식
n과 m이 공백을 사이에 두고 주어집니다.

- 1 ≤ n, m ≤ 100

</br>

## 출력 형식
숫자로 채워진 완성된 형태의 n * m 크기의 사각형을 출력합니다.

(숫자끼리는 공백을 사이에 두고 출력합니다.)

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
n, m = tuple(map(int, input().split()))

array = [
    [0 for _ in range(m)]
    for _ in range(n)
]

num = 1
for i in range(m):
    for j in range(min(i+1, n)):
        array[j][i-j] = num
        num += 1

for i in range(1, n):
    for j in range(min(m, n-i)):
        array[j+i][m-j-1] = num
        num += 1

for row in array:
    for element in row:
        print(element, end=" ")
    print()
```

</div>
</details>