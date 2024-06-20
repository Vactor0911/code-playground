# 문자열 나누기
> 보통

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [문자열 나누기](https://www.codetree.ai/missions/4/problems/divide-string/description "문자열 나누기")

</br>

공백과 숫자로만 이루어진 문자열과 그 문자열의 개수가 주어지면 다섯 개의 숫자씩 나누어서 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 숫자로만 이루어진 문자열의 개수 n이 주어집니다.

두 번째 줄에 10개 이하의 숫자로 이루어진 n개의 문자열이 공백을 사이에 두고 주어집니다.

- 1 ≤ n ≤ 10

- 0 ≤ 주어지는 정수 ≤ 1,000

</br>

## 출력 형식
주어진 문자열을 순서대로 각 줄에 숫자를 5개씩 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
loops = int(sys.stdin.readline())
array = tuple(map(str, sys.stdin.readline().split()))
strBuffer = ""

for i in range(loops):
    strBuffer += array[i]
    if len(strBuffer) >= 5:
        print(strBuffer[:5])
        strBuffer = strBuffer[5:]
print(strBuffer)
```

</div>
</details>