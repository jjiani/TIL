#  데이터 타입(Data Type)

# Number

### 1. Int(정수, ingteger)

- 여러 진수 표현이 가능하다.

``` python
binary_number = 0b10
octal_number = 0o10
decimal_number = 10
hexadecimal_number = 0x10
print(f"""
2진수 : {binary_number}
8진수 : {octal_number}
10진수 : {decimal_number}
16진수 : {hexadecimal_number}
""")
```



### 2. Float(부동소수점, 실수, floating point number)

: 다만, 실수를 컴퓨터가 표현하는 과정에서 부동소수점을 사용하며, 항상 같은 값으로 일치되지 않는다(floating point rounding error) -> 대부분의 경우는 중요하지 않으나 값이 같은지 비교하는 과정에서 문제발생 가능.

- e(E)를 사용할 수도 있다.

```python
pi = 314e-2
print(pi, type(pi))
# 3.14 <class 'float'>
```

- 실수를 연산할때는 위에서 말한 차이가 발생한다. 

``` python
# (1)
a = 5.5 - 5.15
b = 0.35
abs(a - b) <= 1e-10
#True

# (2)sys 모듈사용. epsilon은 부동소수점 연산에서 반올림을 함으로써 발생하는 오차 상환
import sys
abs(a - b) <= sys.float_info.epsilon
#True

# (3)
import math
math.isclose(a, b)
#True
```



### 3. Complex(복소수)

: 실수부(i)와 허수부(j)를 가진다.  문자열로 반환할 시 공백포함 X

```python
complex(1 + 3j)
complex('1+3j')
complex('1 + 3j') # ValueError: complex() arg is a malformed string
```



## String

- 문자열 안에 문장부호(`'`, `"`)가 사용될 경우 이스케이프 문자(`\`)를 활용 가능.

```python
print('Jason said. "Hello?"')
print('Jason said. \'Hello?\'') 
```

- 여러줄에 걸친 문장일 경우 반드시 `"""`를 사용.

- 문자열 또한 `+`연산자와 `*` 연산자 사용이 가능.

```python
'Hello' * 10
'Hello' + 'Jason'
```

- 변수화 또한 가능.

```python
a = 'hello'
b = ', Jason'
a + b
#'hello, Jason'
```

- end 옵션을 사용하면 그 뒤의 출력값과 이어서 출력된다 = 줄바꿈이 안됨.
- `print`는 기본이 줄바꿈!

```python
print('Hello', end='!')
print('Jason')
#'Hello! Jason'
```



## 이스케이프 시퀀스

: 문자열을 활용하는 경우 특수문자 혹은 조작을 하기 위하여 사용되는 것으로 `\`를 활용하여 이를 구분한다.

| 예약문자 |    내용(의미)     |
| :------: | :---------------: |
|    \n    |      줄 바꿈      |
|    \t    |        탭         |
|    \r    |    캐리지리턴     |
|    \0    |     널(Null)      |
|    \\    |        `\`        |
|    \'    | 단일인용부호(`'`) |
|    \"    | 이중인용부호(`"`) |



## String interpolation 

### 1. %-formatting

- %d : 정수/ %f : 실수/ %s : 문자열

```python
name = 'Jason'
score = 3.8

print('Hello, %s' % name)
print('My grade is %d' % score)
print('My grade is %f' % score)
```

### 2. str.format()

```python
print('Hello, {}. My grade is {}'. format(name, score))
```

### 3. f-stirng

```python
print(f'Hello, {name}. My grade is {score}')
```

- 연산과 출력형식 지정도 가능

```python
pi = 3.141592
print(f'원주율은 {pi:.4}이다. 반지름이 5일때 원의 넓이는 {pi*5*5}')
```



## Boolean

-  `True`와 `False`로 구성. 비교/논리 연산을 수행 등에서 활용된다.

- 다음은 `False`로 변환된다. `0, 0.0, (), [], {}, '', None`

- `None`타입 : 값이 없음을 표현



## 형변환(Type conversion)

- 암시적 : 파이썬 내부적으로 자동으로 형변환(bool과 numbers만)

``` python
True + 4 #5
```

- 명시적 

```python
#(1) - string->integer : 형식에 맞는 숫자만 가능!
a = '3.5'
int(a) #ValueError: invalid literal for int() with base 10: '3.5'
a = 3.5
int(a) #3
#(2) - integer->string : 모두 가능
```