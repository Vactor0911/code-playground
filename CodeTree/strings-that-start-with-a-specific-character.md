# 특정 문자로 시작하는 문자열
> --

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [특정 문자로 시작하는 문자열](https://www.codetree.ai/missions/4/problems/strings-that-start-with-a-specific-character/description "특정 문자로 시작하는 문자열")

</br>

알파벳 소문자로 이루어진 n개의 문자열이 주어지고, 알파벳 한 개가 주어졌을 때, 해당 알파벳으로 시작하는 문자열의 개수와 그 문자열들의 길이의 평균을 구하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 정수 n이 주어집니다.

두 번째 줄부터 n개의 줄에 걸쳐, 각 줄에 알파벳 소문자로 이루어져있는 문자열이 하나씩 주어집니다.

n + 2 번째 줄에는 문자의 조건에 해당하는 알파벳 소문자가 하나 주어집니다.

- 1 ≤ n ≤ 20

- 1 ≤ 각 문자열의 길이 ≤ 20

단, 해당 알파벳으로 시작하는 문자열은 반드시 하나 이상 존재합니다.

</br>

## 출력 형식
첫 번째 줄에, 문제의 조건에 해당하는 문자열의 개수와 그 문자열들의 길이의 평균을 공백을 두고 출력합니다.

단, 문자열 길이의 평균값은 소수점 둘째자리까지 반올림하여 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys

loops = int(sys.stdin.readline())
array = [
    sys.stdin.readline().strip()
    for _ in range(loops)
]
char = sys.stdin.readline().strip()

count = length = 0
for k in array:
    if k[0] == char:
        count += 1
        length += len(k)
print("{0} {1:.2f}".format(count, length / count))
```

</div>
</details>