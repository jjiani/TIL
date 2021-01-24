# PYTHON 기초

## 코드라인

- 주석은 `#`으로 표현

  - 여러줄에 걸쳐 주석을 만들고자 할 때에는` """ `또는` '''`으로 묶어준다.

- 한줄로 표기할때는` ;`을 작성하여 표기 가능.

  ```python
  print('hello');print('world')
  ```


``` python
print('hello
world') # 불가능
print('hello\
world') # 가능
print("""hello
world""") #관례적 표현
```

## 변수/ 할당 연산자(Assignment Operator)

- 변수는 `=`을 통해 할당(assignment)된다.
- 해당 데이터 타입을 확인하기 위해서 `type()` 을 활용한다. 
- 같은 값을 동시에 할당 가능하다.

``` python
x = y = 5
print(x, y) #10, 10
```

- 동시에 두개의 변수에 값 두개를 할당 가능.

``` python
x, y = 5, 10
print(x, y) #5, 10
```

- 변수의 개수가 더 많을 때 어떤 오류가 날까?

```python
a, b, c = 5, 10

#ValueError: not enough values to unpack (expected 3, got 2)
```

- 변수의 개수가 더 적다면 어떤 오류가 날까?

``` python
a, b = 5

# TypeError: cannot unpack non-iterable int object
```

- 변수의 값을 서로 바꿀 수 있을까?

``` python
x = 5
y = 10

#(1) - 임시 변수 활용하기
temp = x
x = y 
y = temp
print(x, y)

#(2) - 파이썬스러운 방법
x, y = y, x
print(x, y)
```

## 식별자 (Identifiers)

: 변수, 함수, 모듈, 클래스 등을 식별하는데 사용되는 이름이다.

- 사용할수 없는 식별자가 있다.

```python
import keyword
print(keyword.kwlist)
# ['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

- 내장함수나 모듈 등의 이름으로 만들면 안된다.









