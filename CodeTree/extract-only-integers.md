# 정수만 추출하기
> 보통

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [정수만 추출하기](https://www.codetree.ai/missions/4/problems/extract-only-integers/description "정수만 추출하기")

</br>

공백을 포함하지 않는 두 개의 문자열이 주어지면 앞에서부터 정수 이외의 문자가 나오기 전까지의 부분에서 정수로 변환 가능한 부분을 변환한 후 두 수의 합을 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 길이가 8 이하인 두 개의 문자열이 사이에 공백을 두고 주어집니다. 단, 첫 번째, 두 번째 문자열의 앞 부분에는 최소 1개 이상의 숫자가 주어진다고 가정해도 좋습니다.

</br>

## 출력 형식
첫 번째 줄에 두 문자열에서 추출 가능한 정수 부분의 합을 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
a, b = map(str, input().split())
aryInput = {a, b}

temp = ""
answer = 0
for k in aryInput:
    for l in k:
        if l.isdigit():
            temp += l
        else:
            answer += int(temp)
            temp = ""
            break
    if temp != "":
        answer += int(temp)
        temp = ""
print(answer)
```

</div>
</details>