# 부분 문자열의 개수
> --

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [부분 문자열의 개수](https://www.codetree.ai/missions/4/problems/number-of-substrings/description "부분 문자열의 개수")

</br>

두 문자열 A와 B가 주어졌을 때, 문자열 B가 문자열 A의 부분 문자열로써 등장하는 횟수를 구하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 문자열 A가 주어집니다.

두 번째 줄에 문자열 B가 주어집니다.

단, 문자열 B의 길이는 항상 2임을 가정하여도 좋습니다.

- 1 ≤ 문자열 A의 길이 ≤ 1,000

</br>

## 출력 형식
첫 번째 줄에, 문자열 B가 문자열 A의 부분 문자열로써 등장하는 횟수를 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
strInput = sys.stdin.readline().strip()
strPart = sys.stdin.readline().strip()
lenPart = len(strPart)
count = 0

for i in range(len(strInput) - lenPart + 1):
    if strInput[i:i+lenPart] == strPart:
        count += 1

print(count)
```

</div>
</details>