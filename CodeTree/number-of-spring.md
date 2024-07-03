# 문자열의 개수
> 보통

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [문자열의 개수](https://www.codetree.ai/missions/4/problems/number-of-spring/description "문자열의 개수")

</br>

알파벳으로 이루어진 문자열이 계속 주어지다가 '0'이 주어지면 입력을 종료하고 숫자 0이 주어지기 전까지의 문자열의 개수를 출력하고 홀수 번째 주어진 문자열을 한 줄에 1개씩 출력하는 프로그램을 작성해보세요. 단, '0'은 무조건 주어진다고 가정해도 좋습니다.

</br>

## 입력 형식
각 줄에 문자열이 한 줄에 하나씩 주어집니다. 마지막 줄에는 0이 주어집니다.

- 1 ≤ 주어지는 각 문자열의 길이 ≤ 200

- 1 ≤ 주어지는 총 문자열의 수 ≤ 200

</br>

## 출력 형식
첫 번째 줄에 입력받은 모든 문자열의 개수를 출력하고

두 번째 줄부터 홀수 번째로 주어진 문자열을 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
aryInput = []
while(True):
    string = input()
    if string == "0":
        break
    aryInput.append(string)

print(len(aryInput))
for i in range(0, len(aryInput), 2):
    print(aryInput[i])
```

</div>
</details>