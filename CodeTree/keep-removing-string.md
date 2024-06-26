# 문자열 계속 지우기
> 어려움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [문자열 계속 지우기](https://www.codetree.ai/missions/4/problems/keep-removing-string/description "문자열 계속 지우기")

</br>

문자열 A와 문자열 B가 주어지면 문자열 A의 부분문자열 중 가장 앞에 등장하는 B와 같은 문자열을 찾아 지우려고 합니다. 지우고 난 후 떨어져있는 A의 문자열들을 다시 붙여 만들어진 새로운 문자열에서 부분 문자열 B가 없을 때까지 지우는 것을 반복합니다.

예를 들어 문자열 A가 baabba, B가 ab라면 다음의 과정을 따르게 됩니다.

1. A의 3번째 위치에서 시작하여 4번째 위치에서 끝나는 부분 문자열이 최초로 B와 일치하는 문자열이므로 해당 문자열을 A에서 삭제합니다. baabba → baba
2. 새로 만들어진 문자열 baba에서 2번째 위치에서 시작하여 3번째 위치에서 끝나는 부분 문자열이 최초로 B와 일치하는 문자열이므로 해당 문자열을 삭제합니다. baba → ba
3. 남은 문자열 ba의 연속 부분문자열 중 문자열 B와 일치하는 문자열이 존재하지 않으므로 최종 결과는 ba가 됩니다.

최종적으로 남게 된 문자열을 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에는 문자열 A가 주어집니다.

두 번째 줄에는 문자열 B가 주어집니다.

- 1 ≤ 문자열 A의 길이, 문자열 B의 길이 ≤ 100

</br>

## 출력 형식
문자열 A에서 문자열 B를 찾아 계속 지우는 것을 반복한 이후에 남게되는 문자열을 출력합니다.

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

while strPart in strInput:
    strInput = strInput.replace(strPart, "", 1)
print(strInput)
```

</div>
</details>