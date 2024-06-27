# 소문자와 숫자
> 쉬움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [소문자와 숫자](https://www.codetree.ai/missions/4/problems/letter-and-number/description "소문자와 숫자")

</br>

문자열이 주어지면 영문자와 숫자만 출력하되, 영문자는 모두 소문자로 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 길이가 100 이하인 문자열이 주어집니다.

</br>

## 출력 형식
소문자인 영문자와 숫자로만 이루어진 문자열을 첫 번째 줄에 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
strInput = input()

for k in strInput:
    if k.isalpha() or k.isdigit():
        print(k.lower(), end="")
```

</div>
</details>