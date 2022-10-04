---
layout: page
title: "파이썬 문법"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

## 파이썬 기초 문법

### 리스트 컴프리헨션 

### f-string
```py
print(f"stage {i}: {count/players}%")
```

### 언더바
- 변수의 값을 사용하지 않고 반복할 떄 사용한다.
```py
for _ in range(5):
    print("Hello World!")
```

### set
- 집합 
- 중복 제거 시 사용

### count
**[리스트].count(<요소>)**
=> 리스트안에 있는 요소의 개수를 알려준다.

### append
### sort
- 원본을 변경한다.

### sorted
- 원본을 변경하지 않는다.

reverse
key
key reverse

### reverse
### remove

### insert

### input
### split
### map
```py
data = list(map(int, input("입력: ").split()))
print(data)
```
=> 입력: 1 2 3 4 5<br>
   [1, 2, 3, 4, 5]

#### sys.stdin.readline & rstrip
- 사용자로부터 입력을 빠르게 받아야 하는 경우 사용한다.

```py
import sys

data = sys.stdin.readline().rstrip()
print(data)
```


### try except

### lambda
- 익명 함수로써 한줄로 간단하게 작성할 수 있다.

예시.1 기본

```py
lambda(x,y: x + y)(10,20)
```
=> 30

예시.2 리스트
```py
array = [('a',4),('b',7),('c',3)]

def my_key(x):
    return x[1]
print(sorted(array, key=my_key))

print(sorted(array, key=lambda x: x[1]))
```
=> 2개 모두 같은 결과값을 갖는다.

예시.3 딕셔너리
```py
array = {'a':4,'b':7,'c':3}

def my_key(x):
    return x[1]
print(sorted(array, key=my_key))

print(sorted(array, key=lambda x: array[x]))
```

### is
#### isNaN
#### isDigit
####

### ord & chr
**ord(문자)**
ord('a') => 97

**chr(숫자)**
chr('97') => a

## 라이브러리
### itertools
- 반복되는 형태의 데이터를 처리하기 위한 기능들을 제공한다.

#### 순열 & 조합
##### 순열 nPr
- 서로 다른 n개에서 서로 다른 r개를 선택하여 일렬로 나열
`from itertools import permutations`

중복 순열
`from itertools import product`

##### 조합 nCr
- 서로 다른 n개에서 순서 상관 없이 서로 다른 n개를 선택
`from itertools import combinations`

중복 조합
`from itertools import combinations_with_replacement`

### collections
- deque, conter 등의 자료구조를 포함한다.
#### counter
- 등장 횟수을 세는 기능을 제공한다.
`from colllections import Counter`

### heapq
- 힙 자료구조를 제공한다.

### bisect
- 이진 탐색 기능을 제공한다.

### math
- 수학적 기능을 제공한다.
#### 최대 공약수 & 최대 공배수
-
`import math`
##### 최대 공약수
- 공통된 약수 중에서 제일 큰 수
gcd
##### 최소 공배수
- 공통된 배수 중에서 가장 작은 수
lcm

