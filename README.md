# pythonprc
파이썬 공부
```python
# 함수의 블록구조가 {}가 아닌 indent(들여쓰기) 로구분한다.

if condition:
    print("Hello, World!")

# 코드를 마칠때 별도의 기호가 필요없다. 줄 바꿈으로 구분
x = 10

# JS와 마찬가지로 기본적으로는 변수가 동적타입이다.
x = 10  # Integer
y = "Hello"  # String

# 함수 선언 예약어는 def 이고, {}는 :기호가 대모두 대체하는 듯하다.
def greet():
    print("Hello!")

# class예약어는 동일 근데 constructor 선언 부분이 __init__이고 js의 this가 self 로 대체되는듯?
# 그리고 js의 this 키워드 같은 경우엔 생성자에서 별도 파라미터로 넣어주지 않았는데 파이썬에서는 명시적으로 첫번째 매개변수로 할당해줘야한다.
class Person:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        print(f"Hello, my name is {self.name}")


#js의 변수범위와 달리 키워드가 따로 존재하지않고 전역 or 함수 스코프 2개의 개념만 존재하는듯 하다.
def example():
    x = 10  # 함수 스코프
    if True:
        y = 20  # 여전히 함수 스코프
    print(y)  # 20 출력 가능

# 클로저 개념도 비슷한듯하다. 클로저 개념은 예전에 기억하기론 함수내의 함수가 존재할때 자신이 정의된 위치를 기억하고 자신의 상위함수 변수에 접근할수 있는개념으로 기억하는데 다시 리마인드 할 필요가 있을듯?
def outer():
    x = 10
    def inner():
        print(x)  # x를 참조
    return inner
inner_func = outer()
inner_func()  # 10 출력
```
계속 내용추가 하자 현재까지 원래쓰던 JS와의 차이는 이정도인듯 하다 JS에 참조타입도 궁금해서 검색해봤는데 완전같은 개념인지는 모르겠으나, 어쩄든 어느정도 일맥상통하는 부분이 있어보인다. 얇은, 깊은 복사 개념이 존재한다 추후 내용정리되면 이문구는 삭제
