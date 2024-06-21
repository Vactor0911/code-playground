# 부분문자열 위치 구하기
> 어려움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [부분문자열 위치 구하기](https://www.codetree.ai/missions/4/problems/find-location-of-substring/description "부분문자열 위치 구하기")

</br>

주어진 입력 문자열에 대하여 목적 문자열이 부분 문자열로 존재하는 경우, 부분 문자열의 시작 인덱스를 출력하는 코드를 작성해보세요. 인덱스는 0부터 시작한다고 가정합니다.

</br>

## 입력 형식
첫 번째 줄에는 입력 문자열이 주어지고,

두 번째 줄에는 목적 문자열이 주어집니다.

- 1 ≤ 목적 문자열의 길이(M) ≤ 입력 문자열의 길이 (N) ≤ 1,000

</br>

## 출력 형식
주어진 입력 문자열에 대하여 목적 문자열이 부분 문자열로 존재하는 경우, 부분 문자열의 시작 인덱스를 출력하고, 목적 문자열이 부분 문자열로 존재하지 않는 경우 -1을 출력합니다. 단 목적 문자열이 입력 문자열 내에 여러 번 나타나는 경우, 가장 앞선 인덱스를 출력해줍니다.

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

index = -1

for i in range(len(strInput) - lenPart + 1):
    if strInput[i:i+lenPart] == strPart:
        index = i
        break

print(index)
```

</div>
</details>