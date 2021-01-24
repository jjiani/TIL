# Container

: 여러개의 값을 저장할 수 있는 것

## Sequence형 컨테이너

: 시퀀스는 데이터가 순서대로 나열된 형식을 나타낸다.

** 순서대로 나열 != 정렬

- 특징

1. 순서를 가질 수 있다.
2. 특정 위치의 데이터를 가리킬 수 있다.



### List

- 리스트는 대괄호`[]` 및 `list()`를 통해 만들 수 있다.
- 값에 대한 접근은 `list[i]`로 한다. -> [value1, value2, value3] : 0부터 시작!

### Tuple

- 튜플은 리스트와 유사하지만, `()`로 묶어서 표현합니다. -> (value1, value2)
- 그리고 tuple은 수정 불가능(불변, immutable)하고, 읽을 수 밖에 없습니다. - 주로 직접사용 X

``` python
# (1) 리스트는 특정 원소를 변경할 수 있습니다.
a_list = [5, 10]
a_list[0] = '0번째'
print(my_list)
#['0번째', 10]

# (2) 튜플은 변경 불가능합니다.
b_tuple = (5, 10)
b_tuple[0] = '0번째'
print(my_tuple)
#TypeError: 'tuple' object does not support item assignment
```



### Range

- 기본형 : `range(n)` : 0부터 n-1까지 값을 가짐

- 범위 지정 : `range(n, m)` : n부터 m-1까지 값을 가짐

- 범위 및 스텝 지정 : `range(n, m, s)` : n부터 m-1까지 +s만큼 증가한다.( 음수지정가능)



## 시퀀스에서 활용하는 연산자/함수

|  operation   |          설명           |
| :----------: | :---------------------: |
|   x `in` s   |    containment test     |
| x `not in` s |    containment test     |
|  s1 `+` s2   |      concatenation      |
|   s `*` n    | n번만큼 반복하여 더하기 |
|    `s[i]`    |        indexing         |
|   `s[i:j]`   |         slicing         |
|  `s[i:j:k`]  |    k간격으로 slicing    |
|    len(s)    |          길이           |
|    min(s)    |         최솟값          |
|    max(s)    |         최댓값          |
|  s.count(x)  |        x의 개수         |

```python
# 0(첫번째 값), 전체길이만큼
# 5씩 증가시켜서 slicing
a_list[0:len(a_list):5]

# 0(첫번째 값)
# 5씩 증가시켜서 slicing
sample_list[0::3]
```



## Non-sequence 컨테이너

### Set

- `set`은 수학에서의 집합과 동일하게 처리된다. -> {value1, value2, value3}
- `set`은 중괄호`{}`를 통해 만들며, 순서가 없고 중복된 값이 없다. 

```python
# set으로 중복된 값을 제거
list_a = [2, 1, 2, 3, 1, 1, 2]
list(set(list_a))
# [1, 2, 3] -> 순서보장 X
```

- 빈 집합을 만들려면 `set()`을 사용해야 합니다. (`{}`로 사용 불가능.) 

### Dictionary

: `dictionary`는 `key`와 `value`가 쌍으로 이뤄져있다.

- `{}`를 통해 만들며, `dict()`로 만들 수도 있다. -> {Key1:Value1, Key2:Value2, Key3:Value3, ...}
- `key`는 **변경 불가능(immutable)한 데이터**만 가능. (immutable : string, integer, float, boolean, tuple, range)
- `value`는 `list`, `dictionary`를 포함한 모든 것이 가능하다.

- 중복된 key는 존재 불가능하다.
- 인덱스(0,1,2...)가 아니라 key값으로 접근한다! -> Value값으로 key를 찾을수는 없음!

```python
phone = {'서울': '02', '충북': '043', '대전':'042'}
phone['충북']
#043
```

- 딕셔너리의 .keys() 메소드를 활용하여 key를 확인 해볼 수 있다.
- 딕셔너리의 .values() 메소드를 활용하여 value를 확인 해볼 수 있다.

- 딕셔너리의 .items() 메소드를 활용하여 key, value를 확인 해볼 수 있다. -> (key,value)가 튜플로 묶인 원소를 가진 유사리스트의 형태! -> 인덱스 접근 가능!

