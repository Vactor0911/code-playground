# 알파벳 지우기
> 보통

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [알파벳 지우기](https://www.codetree.ai/missions/4/problems/remove-alphabet/description "알파벳 지우기")

</br>

알파벳과 숫자로 이루어진 문자열이 두 개 주어지면, 각 문자열에서 알파벳을 제외하고 남은 숫자부분을 차례대로 이어붙여 만든 수를 구하고, 두 문자열에서 구한 두 수의 합을 구하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 첫 번째 문자열이 주어집니다.

두 번째 줄에 두 번째 문자열이 주어집니다.

단, 문자열은 알파벳과 숫자로 이루어져 있고, 두 문자열 모두 최소 하나 이상의 숫자를 포함하고 있으며, 문자열 내에서 처음으로 등장한 숫자는 0이 아님을 가정하여도 좋습니다.

- 1 ≤ 문자열의 길이 ≤ 8

</br>

## 출력 형식
첫 번째 줄에 두 문자열에서 구한 두 수의 합을 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
aryInput = [
    input()
    for _ in range(2)
]

temp = ""
answer = 0
for k in aryInput:
    for l in k:
        if l.isdigit():
            temp += l
    answer += int(temp)
    temp = ""
print(answer)
```

</div>
</details>