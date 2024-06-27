# 대문자 소문자 바꾸기
> 쉬움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [대문자 소문자 바꾸기](https://www.codetree.ai/missions/4/problems/change-uppercase-and-lowercase/description "대문자 소문자 바꾸기")

</br>

알파벳으로 이루어진 문자열이 하나 주어지면, 대문자는 소문자로, 소문자는 대문자로 바꾸어 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 알파벳으로 이루어진 문자열이 하나 주어집니다.

- 1 ≤ 문자열의 길이 ≤ 20

</br>

## 출력 형식
첫 번째 줄에, 입력된 문자열에서 대문자는 소문자로, 소문자는 대문자로 바꾸어 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
strInput = input()

for k in strInput:
    if k.isupper():
        print(k.lower(), end="")
    else:
        print(k.upper(), end="")
```

</div>
</details>