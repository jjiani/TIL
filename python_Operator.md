# 연산자(Operator)

## 산술 연산자

| 연산자 |      내용      |
| :----: | :------------: |
|   +    |      덧셈      |
|   -    |      뺄셈      |
|   *    |      곱셈      |
|   /    |     나눗셈     |
|   //   |       몫       |
|   %    | 나머지(modulo) |
|   **   |    거듭제곱    |

- `/`은 항상 float를 돌려준다.
- 정수 나눗셈 으로 정수 결과(소수X)를 얻으려면 `//` 연산자를 사용한다.



## 비교연산자

|  연산자  |          내용          |
| :------: | :--------------------: |
|   `<`    |          미만          |
|   `<=`   |          이하          |
|   `>`    |          초과          |
|   `>=`   |          이상          |
|   `==`   |          같음          |
|   `!=`   |        같지않음        |
|   `is`   |    객체 아이덴티티     |
| `is not` | 부정된 객체 아이덴티티 |



## 논리연산자

| 연산자  |             내용             |
| :-----: | :--------------------------: |
| a and b |   a와 b 모두 True시만 True   |
| a or b  | a 와 b 모두 False시만 False  |
|  not a  | True -> False, False -> True |

```python
print(True1 and True2) # True2
print(True1 and False1) # False1
print(False1 and True1) # False1
print(False1 and False2) # False1
```

```python
print(True1 or True2) # True1
print(True1 or False1) #True1
print(False1 or True1) #True1
print(False1 or False2) #False2
```

```python
print(not True) #False
print(not 0) #True
```



## 복합연산자

| 연산자  |    내용    |
| :-----: | :--------: |
| a += b  | a = a + b  |
| a -= b  | a = a - b  |
| a *= b  | a = a * b  |
| a /= b  | a = a / b  |
| a //= b | a = a // b |
| a %= b  | a = a % b  |
| a **= b | a = a ** b |



## 연산자 우선순위

1. `()`을 통한 grouping
2. Slicing
3. Indexing
4. 제곱연산자 `**`
5. 단항연산자 `+`, `-` (음수/양수 부호)
6. 산술연산자 `*`, `/`, `%`
7. 산술연산자 `+`, `-`
8. 비교연산자, `in`, `is`
9. `not`
10. `and`
11. `or`