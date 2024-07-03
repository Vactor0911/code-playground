# 문자열 거꾸로 출력하기
> 쉬움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [문자열 거꾸로 출력하기](https://www.codetree.ai/missions/4/problems/print-string-backward/description "문자열 거꾸로 출력하기")

</br>

알파벳으로 이루어진 문자열이 주어지면 거꾸로 뒤집어 출력하기를 반복하다가 'END'가 주어지면 작업을 종료하는 프로그램을 작성해보세요. 단, 'END'는 무조건 10번 이내에 주어진다고 가정해도 좋습니다.

</br>

## 입력 형식
첫 번째 줄부터 길이가 100 이하인 문자열이 각 줄마다 주어집니다. 마지막 줄에는 'END'가 주어집니다.

</br>

## 출력 형식
첫 번째 줄부터 각 줄마다 주어진 문자열을 거꾸로 뒤집어 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
while(True):
    string = input()
    if string == "END":
        break
    listString = list(string)
    listString.reverse()
    print("".join(listString))
```

</div>
</details>