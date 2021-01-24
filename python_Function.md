# Function 1

##  함수 : 특정한 기능을 하는 코드의 묶음

- 높은 가독성 = 짧아짐
- 재사용성
- 유지보수 : 코드의 기능별 분화

## 함수의 선언과 호출

- 함수 선언은 `def`로 시작하여 `:`으로 끝나고, 다음은 ` tab(들여쓰기)`로 코드 블록을 만든다.

- 함수는 `parameter(매개변수)`를 넘겨줄 수도 있다.

- 함수는 동작후에 `return`을 통해 결과값을 전달 할 수도 있다. (`return` 값이 없으면, `None`을 반환한다.)

- 함수는 호출을 `func()` / `func(val1, val2)`와 같이 한다.

```python
def 함수이름(parameter1, parameter2) :
    코드블럭
    return value
```

```python
def m_sum(a, b) :
    return a + b

number = m_sum(1,3)
print(number) #4

#cf
n_number = print(7+3)
print(n_number) #None -> print함수는 None을 반환하고 print_number변수에 None이 저장됨

#correct
n_number = 7 + 3
print(n_number) #10
```



## 함수의 Output

### Return :

- 함수는 반환되는 값이 있으며 어떠한 종류라도(str, int, list ...) 상관없다.

- 그러나 오직 한 개의 객체만 반환된다 = 여러개의 인자를 받고싶다면 다른 자료구조를 이용 

- 함수가 return되거나 종료되면, 함수를 호출한 곳으로 돌아간다. 

- return은 함수안의 내용을 함수 밖으로 내보내기 위한 마침표 같은것! 규칙이다!

- 따라서 함수에서 아무것도 return 하지 않으면 None이 반환된다.

  





