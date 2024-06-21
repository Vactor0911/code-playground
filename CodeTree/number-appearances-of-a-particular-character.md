# 특정 문자의 등장 횟수
> 쉬움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [특정 문자의 등장 횟수](https://www.codetree.ai/missions/4/problems/number-appearances-of-a-particular-character/description "특정 문자의 등장 횟수")

</br>

문자열이 주어지면 주어진 문자열에 'ee', 'eb'가 각각 몇 번씩 나왔는지를 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 소문자 알파벳으로만 이루어졌고 길이가 20 이하인 문자열이 주어집니다.

</br>

## 출력 형식
첫 번째 줄에 'ee', 'eb'가 각각 몇 번씩 나왔는지를 공백을 사이에 두고 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
strInput = sys.stdin.readline().strip()

counts = [0, 0]
string = ["ee", "eb"]
for i in range(len(string)):
    for j in range(len(strInput)-1):
        if strInput[j:j+2] == string[i]:
            counts[i] += 1
print(counts[0], counts[1])
```

</div>
</details>