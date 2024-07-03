# 두 수의 합과 1
> --

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [두 수의 합과 1](https://www.codetree.ai/missions/4/problems/two-nums-sum-and-1/description "두 수의 합과 1")

</br>

두 정수가 주어지면 그 두 수의 합을 더한 뒤의 결과에 숫자 1이 몇 번 나오는지 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 정수 두 정수가 공백을 사이에 두고 주어집니다.

- 1 ≤ 두 정수 ≤ 1,000

</br>

## 출력 형식
첫 번째 줄에 해당하는 정수값을 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
aryInput = tuple(map(int, sys.stdin.readline().split()))

result = str( sum(aryInput) )

answer = 0
for k in result:
    if k == "1":
        answer += 1
print(answer)
```

</div>
</details>