# Python

### 기본 문법 정리

<br>

## String 

- `.upper()` : 모두 대문자로 변환
- `.lower()` : 모두 소문자로 변환
- `.swapcase()` : 소문자는 대문자로, 대문자는 소문자로
- `.replace(기존값, 바꿀값)` : 문자열의 값을 찾아 모두 바꿈
- `.strip(삭제할값)` : 양 옆의 값을 삭제 (r, l 붙여서 양옆 방향 지정 가능)
- `.split(나눌 기준)` : 설정 기준에 따라 문자열을 분리
- `.isalpha()` : 문자열이 알파벳인지 여부 bool 리턴
- `.isdigit()`, `.isnumeric(`) : 문자열이 숫자인지 여부 bool 리턴
- `'구분자'.join(리스트)` : 리스트 요소를 구분자와 함께 모두 붙임

<br>

## List

- `.append(값)` : 리스트 맨 뒤에 해당 값 그 자체를 추가한다. 1개만 추가됨
- `.extend(값)` : 리스트 맨 뒤에 가장 바깥쪽 iterable의 모든 값을 추가한다. (한 단계를 풀어서 넣는다고 생각)
- `.remove(값)` : 리스트를 뒤져서 해당 값을 하나만 삭제 (맨 앞에거)
- `.pop(인덱스)` : 해당 인덱스에 해당하는 값을 삭제 후 반환
- `.index(값)` : 찾는 값에 해당하는 인덱스를 반환
- `.count(값)` : 해당 값의 등장횟수를 리턴
- `.sort(key, reverse)` : 해당 리스트를 정렬

<br>

## Dictionary

- `dict.fromkeys(리스트, default V)` : 해당 리스트를 key, 설정한 값을 value로 딕셔너리 생성
- `.keys()` : key 리스트 리턴
- `.values()` : value 리스트 리턴
- `.items()` : (k, v) 튜플 리스트 리턴
- `.has_key(키값)` : 해당 key 존재여부 bool 리턴 
- `.setdefault(키값, default V)` : 해당 key가 있으면 해당 value 리턴, 없으면 설정한 value 리턴
- `.pop(키값)` : 해당 key 삭제
- `.clear()` : 싹다 삭제

<br>

## ETC

- `min(iterable)`, `max(iterable)` : 요소에 있는 최대,최소값 반환
- `sum(iterable)` : 요소에 있는 값 모두 더한 값 반환
- `sum(2차원리스트, [])` : 2차원리스트 입력시 모두 flatten해서 1차원리스트로 반환.
- `for i, item in enumerate(iterable)` : 요소에 있는 인덱스까지 얻고 싶을때 사용
- `zip(리스트, ...)` : 리스트의 같은 인덱스 요소들을 튜플로 묶어준다.
- `sorted(iterable, key = 함수, reverse = bool)` : 해당 요소를 정렬하고 반환
- `map(함수, iterable)` : 정의된 함수에 따라 해당 요소를 변환

<br>

## deepcopy

```python
import copy
리스트 = copy.deepcopy(복사할 리스트)
```

- 2차원 리스트나 참조 타입은 기존의 `.copy()` 함수로 복사가 되지 않음
    - 따라서 깊은복사 사용

<br>

## heapq

```python
import heapq
heapq.heapify(리스트)
```

- 별도의 자료구조가 아님
- 기존 리스트가 있다면 힙으로 초기화시켜놓고 사용하는게 좋다
- default는 최소 힙임

### 메소드

- `heapq.heapify(리스트)` : 기존 리스트를 힙으로 변경
- `heapq.heappush(리스트, 값)` : 힙에 값 추가
- `heapq.heappop(리스트)` : 힙 최소값(root값) 삭제 후 리턴

<br>

## deque

```python
from collections import deque
# 기존 리스트를 덱으로 만들기
q = deque(리스트)
```

- queue 모듈과 달리 방향성이 존재함
- 데이터 삽입/삭제는 O(1), 무작위접근은 O(N)

### 메소드

- `.popleft()` : 왼쪽 값 pop
- `.popright()` : 오른쪽 값 pop
- `.appendleft(값)` : 왼쪽 값 append
- `.append(값)` : 오른쪽 값 append
- `.remove('값')` : 왼쪽부터 검사하여 가장 먼저 나타나는 값 삭제

<br>

## Counter

```python
from collections import Counter
딕셔너리 = Conter(리스트)  
```

- 리스트의 값이 key, 등장횟수가 value인 딕셔너리 반환
- 딕셔너리와 메소드 동일

### 메소드

- `.most_common()` : 카운트가 많은순으로 정렬 (내림차순)
- `.elements()` : 카운터 변환 전 리스트로 변환
- `카운터1.update(카운터2)` : 카운터 간 count 덧셈
- `카운터1.subtract(카운터2)` : 카운터 간 count 뺄셈
    - 카운터 간 연산은 그냥 연산자 사용해서 해도 됨

<br>

## defaultdict

```python
from collections import defaultdict
딕셔너리 = defaultdict(타입)
딕셔너리 = defaultdict(lambda : ...) 
```

- key만 넣어도 value가 자동 생성
- 타입은 `int`, `list` 등 입력
- lambda로 특정 타입 지정 

<br>

## combinations / permutations

```python
from itertools import combinations, permutations
combinations(대상리스트, 원소 수)
permutations(대상리스트, 원소 수)
# ex)
리스트.extend(combinations(대상리스트, 원소 수))
```

- 입력된 원소 수에 하는 조합/순열을 반환
- 반환형이 리스트가 아니라서 extend로 리스트에 담는 방식으로 활용함

<br>

## datetime

```python
from datetime import datetime, timedelta
```

### 메소드

- `datetime.strptime(문자열, 형식)` : 문자열을 시간 데이터로 파싱
    - 형식 ex) %Y-%m-%d %H:%M:%S.%f
- `datetime.timedelta(시간단위 = 추가할 시간)` : 숫자 자료형을 원하는 시간단위로 시간 데이터로 파싱

<br>