# Java Collection

### 기본문법 + 자바 컬렉션 문법정리

<br>

## Type 변환

### 메소드

- `리스트.stream().mapToInt(i -> i).toArray()` : List -> Array
- `Integer.toString(int변수)` : int를 String으로 변환
- `Integer.parseInt(str변수)` : String을 int로 변환

<br>

## String

### 기본

```java
// 선언
String str;
String str = new String();
// 선언 + 할당
String str = "";
String str = new String("");
```

- Java 문자열은 C언어나 Python과는 달리 리스트나 배열이 아님
- 리스트나 배열의 length 메소드의 형태가 다름

### 메소드

- `.length()` : 문자열 길이 반환
- `.contains(문자열)` : 입력 문자열이 문자열 안에 포함된다면 true 반환
- `.startsWith(문자열)` : 문자열 시작이 입력 문자열이라면 true 반환
- `.isEmpty()` : 변수가 ''라면 true 반환
- `문자열1.equals(문자열2)` : String 값을 비교할 때 사용한다. 값1과 값2를 비교해서 bool값을 반환해준다.
   - ` == ` : equals는 값 자체를 비교하고 == 은 주소값을 비교한다. int 배열에서는 그냥 == 사용.
- `.indexOf(문자열)` : 해당 문자열이 존재하는 인덱스 반환 / 존재X -> -1 반환
- `.subString(시작인덱스, 끝인덱스)` : 문자열을 인덱스 범위만큼 자름. (입력값이 하나면 그 인덱스부터 끝까지 자름)
- `문자열1.concat(문자열2)` : 문자열 두개를 합침
- `.replace(찾는문자, 바꿀문자)` : 문자열에서 입력 문자를 찾아서 바꿈
- `.split(분리기준)` : 문자열을 기준대로 나누고 String 배열 반환
- `.trip()`, `strip()` : 문자열 앞뒤 공백 제거

<br>

## Arrays

### 기본

```java
// 선언
int[] arr;
int[][] arr2;
// 선언+할당 -> 할당시 default 값은 0으로 초기화됨.
int[] arr = {};
int[] arr = new int[5];
int[][] arr2 = { {1,2}, {3,4} };
int[][] arr2 = new int[2][2]];
// 선언+할당+초기화
int[] arr = new int[]{1,2,3,4,5};

```

- 기본적인 배열, 정적 리스트이다. (길이 변경불가)

### 메소드

- `.length` : 배열 길이 반환
- `Arrays.toString(배열)` : 배열을 문자열로 바꿔줌 (출력용도)
- `Arrays.sort(배열)` : 입력 배열을 정렬해주는 메소드
- `Arrays.copyOf(배열, 복사할 길이)` : 인덱스 0부터 0포함하는 길이만큼 복사한 배열을 반환
- `Arrays.copyOfRange(배열, 시작인덱스, 끝인덱스)` : 시작인덱스(포함)부터 끝인덱스-1 까지 복사한 배열을 반환

<br>

## Collections

### 기본

```java
import java.util.*;
```

- 여러 원소를 담을 수 있는 다양한 자료구조
- List, Set, Queue, Map 인터페이스가 존재하며, 이 인터페이스를 상속해 다양한 컬렉션을 구현한다
- 보통 컬렉션을 print로 출력 시 toString으로 자동 출력된다.

### 메소드

- `.size()` : 컬렉션의 크기를 반환
- `.sort(객체, Comparable)` : 컬렉션 객체를 기준에 따라 정렬. Comparable 객체는 람다식으로 구현한다
- `.reverseOrder()` : sort 나 다른 컬렉션의 초기 인자로 입력되는 메소드. 역으로 정렬해줌

<br>

## ArrayList

### 기본

```java
// 선언 + 할당
List<'자료형'> '이름' = new ArrayList<>();
// 선언 + 할당 + 초기화 -> 초기화시 입력값은 리스트이다.
List<'자료형'> '이름' = new ArrayList<>('리스트');
```

- 배열을 기반으로 구성되어 있는 동적 리스트
- 값 변경 시 임시 배열을 생성, 값들을 복사하는 동작이 일어남
- 탐색에는 효율적, 삽입/삭제에는 비효율적

### 메소드

- `.add(값)` : 값 추가하기 (맨 뒤에 추가됨)
- `.remove(값or인덱스)` : 입력값이나 인덱스에 해당하는 값을 pop
- `.get(인덱스)` : 인덱스에 해당하는 값을 출력
- `.set(인덱스, 바꿀값)` : 인덱스의 값을 바꾸기

<br>

## LinkedList

### 기본

```java
// 선언 + 할당
List<'자료형'> '이름' = new LinkedList<>();
// 선언 + 할당 + 초기화 -> 초기화시 입력값은 리스트이다.
List<'자료형'> '이름' = new LinkedList<>('리스트');
```

- 연결리스트로 구현된 동적 리스트
- 값 변경 시 새 노드만 추가, 삭제해주면 된다.
- 탐색에는 비효율적, 삽입/삭제에는 효율적

### 메소드

- ArrayList와 동일
- `.addFirst(값)` : 가장 앞에 데이터 추가
- `.addLast(값)` : 가장 뒤에 데이터 추가

<br>

## HashSet

### 기본

```java
// 선언 + 할당
Set<'자료형'> '이름' = new HashSet<>();
```

- 집합 컬렉션 (파이썬의 set과 동일함)
- 중복은 제거, 순서 없이 저장됨

### 메소드

- `.size()` : 집합 크기 출력
- `.add(값)` : 입력 값을 집합에 추가
- `.remove(값)` : 입력 값을 삭제
- `.clear()` : 모두 삭제
- `.contains(값)` : 집합에 입력 값이 있다면 true

<br>

## HashMap

### 기본

```java
// 선언+할당
Map<'K자료형', 'V자료형'> '이름' = new HashMap<>();
```
- (키, 값)의 형태로 저장해주는 컬렉션.
- 키는 고유값으로 중복 없음, 순서 없이 저장됨
- 성능 : O(1)

### 메소드

- `.put(K, V)` : 해쉬맵에 키, 값 넣기
- `.get(K)` : 해당 키의 값을 불러온다
- `.remove(K)` : 해당 키의 값을 삭제하고 반환
- `.clear()` : 모든 데이터 삭제
- `.isEmpty()` : 비어있는지 확인후 bool값 반환
- `.keySet()` : 모든 키를 저장한 Set을 반환
- `.values()` : 모든 값을 저장한 컬렉션을 반환(형태가 정해져있지 않다는 것)
- `.entrySet()` : 모든 (키=값) 형태의 Map.Entry을 반환 
    - `.getKey/Value()` : entrySet으로 반환 받았을 경우 키와 값을 따로 받아낼 수 있는 메소드.
- `.containsKey(K)` : 해당 키가 들어있는지 확인후 bool값 반환
- `.containsValue(V)` : 해당 값이 들어있는지 확인후 bool값 반환
- `.replace(K, V)` : 해당 키의 값을 입력 값으로 바꿈

<br>

## TreeMap

### 기본

```java
// 선언+할당
TreeMap<'K자료형', 'V자료형'> '이름' = new TreeMap<>();
```

- 해시맵과 동일하지만 key 순서를 반영
- key값만 정렬이 가능
- 성능 : O(log(n))

<br>

## LinkedHashMap

### 기본

```java
// 선언+할당
LinkedHashMap<'K자료형', 'V자료형'> '이름' = new LinkedHashMap<>();
```

- 해시맵과 동일하지만 입력 순서를 반영해 저장한다.
- key와 value 둘 다 정렬이 가능하다
- 성능 : O(n)

<br>

## Queue

### 기본

```java
// 선언 + 할당
Queue<'자료형'> '이름' = new LinkedList<>();
```

- 큐. 연결리스트로 구현되어있고 인덱스로의 접근이 불가능하다. 

### 메소드

- `.add(값)` , `offer(값)` : 
- `.poll()` : 첫 번째 값을 제거하고 반환 (pop)
- `.remove()` : 첫 번째 값을 제거 
- `.peek()` : 첫 번째 값을 출력(삭제 X)
- `.clear()` : 큐 초기화 (모두 삭제)

<br>

## PriorityQueue

### 기본

```java
// 선언 + 할당
PriorityQueue<'자료형'> '이름' = new PriorityQueue<>();
```

- 우선순위 큐 / 내부는 힙으로 구현되어 있다. (프린트 찍어보면 트리구조로 나옴)
- `Queue` 컬렉션의 메소드와 동일하다.

<br>

