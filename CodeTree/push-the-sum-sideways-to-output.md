# 합을 옆으로 밀어 출력
> --

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [합을 옆으로 밀어 출력](https://www.codetree.ai/missions/4/problems/push-the-sum-sideways-to-output/description "합을 옆으로 밀어 출력")

</br>

n개의 수가 주어질 때, 모든 수를 더한 값을 좌측으로 한 칸 민 결과를 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 입력되는 수의 개수 n이 주어집니다.

두 번째 줄부터 n개의 줄에 걸쳐 수가 하나씩 주어집니다.

- 1 ≤ n ≤ 100

- 10 ≤ 주어지는 수 ≤ 5,000

</br>

## 출력 형식
첫 번째 줄에 모든 수를 더한 값을 좌측으로 한 칸 민 결과를 출력합니다.

단, 출력결과가 0으로 시작하여도 0을 출력하여야 함에 유의합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
loops = int(sys.stdin.readline())
aryInput = [
    int(sys.stdin.readline())
    for _ in range(loops)
]

result = str(sum(aryInput))
print(result[1:] + result[0])
```

</div>
</details>