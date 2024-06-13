# Run Length 인코딩
> 보통

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [Run Length 인코딩](https://www.codetree.ai/missions/4/problems/run-length-encoding/description "Run Length 인코딩")

</br>

문자열 A가 주어졌을 때 문자열 A에 Run-Length Encoding을 적용한 이후의 결과를 구해보려고 합니다. Run-Length Encoding이란 간단한 비손실 압축 방식으로, 연속해서 나온 문자와 연속해서 나온 개수로 나타내는 방식입니다.

예를 들어, 문자열 A가 aaabbbbcbb인 경우 순서대로 a가 3번, b가 4번, c가 1번 그리고 b가 2번 나왔으므로 Run-Length Encoding을 적용하게 되면 a3b4c1b2가 됩니다.

문자열 A가 주어졌을 때, Run-Length Encoding을 적용한 이후의 결과를 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 문자열 A가 주어집니다. 문자열 A는 소문자 알파벳으로만 이루어져 있습니다.

- 1 ≤ 문자열 A의 길이 ≤ 1,000

</br>

## 출력 형식
첫 번째 줄에는 문자열 A에 Run-Length Encoding을 적용한 이후의 길이를 출력합니다.

두 번째 줄에는 문자열 A에 Run-Length Encoding을 적용한 이후의 결과를 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
strInput = sys.stdin.readline().strip()

char = strInput[0]
charcount = 1
answer = ""

for i in range(1, len(strInput)):
    if strInput[i] != char:
        answer += char + str(charcount)
        char = strInput[i]
        charcount = 1
    else:
        charcount += 1
answer += char + str(charcount)

print(len(answer))
print(answer)
```

</div>
</details>