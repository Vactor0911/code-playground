# 미는 횟수
> 보통

|시간 제한|메모리 제한|
|:---:|:---:|
|1초|80 MB|

**문제 바로가기** : [미는 횟수](https://www.codetree.ai/missions/4/problems/number-of-pushes/description "미는 횟수")

</br>

문자열 A를 우측으로 한 칸씩 n번 밀었을 때, 문자열 A 와 문자열 B가 같아지는 순간의 n 중 가능한 최솟값을 구하는 프로그램을 작성해보세요. (n > 0)

</br>

## 입력 형식
첫 번째 줄에 문자열 A가 주어집니다.

두 번째 줄에 문자열 B가 주어집니다.

이때, 문자열 A와 문자열 B의 길이는 같습니다.

단, 처음 문자열 A와 문자열 B는 항상 다르게 주어짐을 가정하여도 좋습니다.

- 2 ≤ 문자열의 길이 ≤ 100

</br>

## 출력 형식
첫 번째 줄에, 문자열 A를 우측으로 한 칸씩 n번 밀었을 때, 문자열 A 와 문자열 B가 같아지도록 하는 n 값 중 가능한 최솟값을 출력합니다. 만약 불가능하다면 -1을 출력합니다.

</br>

## 해답
- **Python3**
<details>
<summary>접기 / 펼치기</summary>
<div markdown="1">

```py
strInput = input()
target = input()

flagError = True
for i in range(len(strInput)):
    if strInput == target:
        print(i)
        flagError = False
        break
    else:
        strInput = strInput[-1] + strInput[:-1]

if flagError:
    print(-1)
```

</div>
</details>