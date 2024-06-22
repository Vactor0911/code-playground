# 문자열 놀이
> 어려움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [문자열 놀이](https://www.codetree.ai/missions/4/problems/play-with-string/description "문자열 놀이")

</br>

문자열 s와 q개의 질의가 주어졌을 때 각 질의를 수행하는 프로그램을 작성해보세요. 단, 질의를 순서대로 수행해야 하며, 문자열은 질의에 따라 계속 변합니다. 질의의 종류는 다음과 같습니다.

- 1 a b

    a번째 문자와 b번째 문자를 교환한 뒤 출력합니다.

- 2 a b

    문자 a를 전부 문자 b로 변경한 뒤 출력합니다.

</br>

## 입력 형식
첫 번째 줄에 문자열 s와 질의의 수를 나타내는 q값이 공백을 사이에 두고 주어집니다.

두 번째 줄 부터는 q개의 줄에 걸쳐 질의가 주어집니다. 각 질의는 다음 2개 중 하나의 타입으로 주어집니다.

(1) 1 a b (1 ≤ a, b ≤ n, a 

= b)

(2) 2 a b (a, b는 소문자 알파벳)

문제에서 주어지는 모든 문자는 전부 소문자 알파벳이라 가정해도 좋습니다.

- 1 ≤ 문자열 s의 길이 ≤ 100
- 1 ≤ q ≤ 100

</br>

## 출력 형식
q개의 질의에 대한 결과를 한 줄에 하나씩 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
aryInput = tuple(map(str, sys.stdin.readline().split()))
strInput = aryInput[0]
loops = int(aryInput[1])

for _ in range(loops):
    command = tuple(map(str, sys.stdin.readline().split()))
    if command[0] == "1":
        listInput = list(strInput)
        idxFrom = int(command[1]) - 1
        idxTo = int(command[2]) - 1

        temp = listInput[idxFrom]
        listInput[idxFrom] = listInput[idxTo]
        listInput[idxTo] = temp
        strInput = "".join(listInput)
        print(strInput)
    else:
        strInput = strInput.replace(command[1], command[2])
        print(strInput)
```

</div>
</details>