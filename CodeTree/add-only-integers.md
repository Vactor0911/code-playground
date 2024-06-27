# 정수만 더하기
> 쉬움

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [정수만 더하기](https://www.codetree.ai/missions/4/problems/add-only-integers/description "정수만 더하기")

</br>

숫자와 알파벳으로 이루어진 문자열 A가 주어졌을 때, 그 중 숫자들만 골라 그 합을 출력하는 프로그램을 작성해보세요.

</br>

## 입력 형식
첫 번째 줄에 숫자와 알파벳으로 이루어진 문자열 A가 주어집니다. 최소 하나 이상의 숫자가 주어짐을 가정해도 좋습니다.

- 1 ≤ 문자열의 길이 ≤ 20

</br>

## 출력 형식
첫 번째 줄에 문자열 A에서 숫자들만 골라 그 합을 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
strInput = input()

answer = 0
for k in strInput:
    if k.isdigit():
        answer += int(k)
print(answer)
```

</div>
</details>