# 문자 제거하기
> 쉬움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [문자 제거하기](https://www.codetree.ai/missions/4/problems/del-char/description "문자 제거하기")

</br>

알파벳으로 이루어진 문자열과 정수가 주어지면, 문자열에서 정수에 해당하는 위치의 문자를 제거하고 출력하는 작업을 반복하다가 문자 1개가 남으면 종료하는 프로그램을 작성해보세요. 만약 주어진 정수가 문자열의 길이 이상이면 마지막 문자를 제거합니다. 위치는 0번부터 주어진다고 가정합니다.

</br>

## 입력 형식
첫 번째 줄에 길이가 20 이하인 문자열이,

두 번째 줄부터 문자가 하나 남을때까지 각 줄에 정수가 주어집니다.

</br>

## 출력 형식
각 줄에 주어진 정수에 해당하는 문자가 지워진 문자열을 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
import sys
listInput = list(sys.stdin.readline().strip())

while len(listInput) > 1:
    index = min( int(sys.stdin.readline().strip()), len(listInput)-1 )
    listInput.pop(index)
    print("".join(listInput))
```

</div>
</details>