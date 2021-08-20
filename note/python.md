# <파이썬 문법 정리>

## 문자열 관련 
- `replace(기존값, 바꿀값)` 
- `strip(삭제할값, )`
- `split(나눌 기준)`

<br>


## 리스트 관련
- `append(값)` : 리스트 맨 뒤에 해당 값 그 자체를 추가한다. 1개만 추가됨
- `extend(값)` : 리스트 맨 뒤에 가장 바깥쪽 iterable의 모든 값을 추가한다. (한 단계를 풀어서 넣는다고 생각)
- `remove(값)` : 리스트를 뒤져서 해당 값을 하나만 삭제 (맨 앞에거)
- `pop(인덱스)` : 해당 인덱스에 해당하는 값을 삭제 후 반환
- `index(값)` : 찾는 값에 해당하는 인덱스를 반환
- `sort(list, key, reverse)` : 해당 리스트를 정렬
- `sorted(list, key, reverse)` : 해당 리스트를 정렬하고 반환
- `sum(리스트)` : 리스트에 있는 값 모두 더한 값 반환

<br>

## 딕셔너리 관련

<br>


## 기타 함수
- `enumerate(zip(리스트))` : zip으로 두 리스트를 묶고 순회하면 튜플로 출력, 그 튜플에 인덱스까지 추출하기
- `sum(2차원리스트, [])` : 2차원리스트 입력시 모두 flatten해서 1차원리스트로 반환.

<br>


## 외부 함수
> ### deque
```python
from collections import deque
q = deque('리스트') # 컬렉션의 내장함수. 리스트를 큐의 형태로 바꿀때 한다.
q.popleft()         # 왼쪽 값 pop
q.popright()        # 오른쪽 값 pop
q.append()          # 오른쪽 값 append
q.remove('값')      # 왼쪽부터 검사하여 가장 먼저 나타나는 값 삭제
```

> ### Counter
```python
from collections import Counter
# 리스트의 값이 key, 등장횟수가 value인 딕셔너리 반환
'딕셔너리' = Conter('리스트')  
```

> ### defaultdict
```python
from collections import defaultdict
'딕셔너리' = defaultdict(int)           # 기본값이 int인 딕셔너리 생성
'딕셔너리' = defaultdict(lambda : [])    # 기본값이 []인 딕셔너리 생성
```

> ### combinations / permutations
```python
from itertools import combinations, permutations
# 입력된 원소 수에 하는 조합/순열을 반환
# 반환형이 리스트가 아니다. extend로 리스트에 담는 방식으로 활용함
combinations('대상리스트', '원소 수')
permutations('대상리스트', '원소 수')
'리스트'.extend(combinations('대상리스트', '원소 수'))  # 리스트에 담기.
```

> ### itemgetter
```python
from operator import itemgetter
# sorted함수 안에서 key의 값으로 사용됨.
# 이차원 리스트일 경우 원소 리스트의 열을 기준으로 정렬된다. (key에 lambda x:x[_] 를 넣은것과 동일)
sorted('이차원리스트', key = itemgetter('정렬 기준 인덱스'))
```

> ### copy
```python
import copy
# 2차원 리스트는 기존의 .copy()함수로 복사가 되지 않는다.
# 따라서 2차원 리스트를 복사하려면 deepcopy 메소드를 사용해야함
'리스트' = copy.deepcopy('복사할 리스트')
```

> ### datetime
```python
from datetime import datetime, timedelta
# 문자열을 시간 데이터로 파싱
datetime.strptime('문자열', '형식')     # 형식 ex) %Y-%m-%d %H:%M:%S.%f
# 숫자 자료형을 원하는 시간단위로 시간 데이터로 파싱
datetime.timedelta('시간단위' = '추가할 시간')
```





