# 규칙에 따라 밀기
> --

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [규칙에 따라 밀기](https://www.codetree.ai/missions/4/problems/push-by-the-rules/description "규칙에 따라 밀기")

</br>

문자열 A가 주어졌을 때, 명령에 따라 문자열 A를 민 결과를 출력하는 프로그램을 작성해보세요.

명령은 L 또는 R 로 이루어진 명령 문자열로 주어지고, 명령에 따라 순서대로 다음을 반복합니다.

- L일 때는 좌측으로 한 칸 밀고, R일 때는 우측으로 한 칸 미는 것을 진행합니다.

</br>

## 입력 형식
첫 번째 줄에 알파벳 소문자로 이루어진 문자열 A가 주어집니다.

두 번째 줄에 L 또는 R 로 이루어진 명령 문자열이 주어집니다.

- 1 ≤ 문자열 A의 길이 ≤ 100

- 1 ≤ 명령 문자열의 길이 ≤ 100

</br>

## 출력 형식
첫 번째 줄에, 주어진 문자열을 명령에 따라 미는 것을 진행한 후 문자열A의 최종 상태를 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
strInput = sys.stdin.readline().strip()
strCommand = sys.stdin.readline().strip()

for k in strCommand:
    if k == "L":
        strInput = strInput[1:] + strInput[0]
    else:
        strInput = strInput[-1] + strInput[:-1]
print(strInput)
```

</div>
</details>