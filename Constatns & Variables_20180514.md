Swift 에서는 (아니 어쩌면 다른 Language 에서도) 사용되는 데이터를 변수와 상수를 이용하여 저장한다.
더욱 쉽게 말하면 변수와 상수는 데이터 타입에 해당하는 값의 이름이다.

Apple Document 인 The Swift Programming Language (Swift 4.1) 에 따르면 상수와 변수를 다음과 같이 정의 하고 있다.

*The value of a constant can't be changed once it's set, whereas a variable can be set to a different value in the future.
Constants and Variables must be declare before they're used.
You declare constants with the let keyword and variables with the var keyword.*

(상수는 한번 선언하면 값을 변경할 수 없고, 변수는 이후에 다른 값으로 다시 선언할 수 있다.
상수와 변수는 사용하기 전에 반드시 선언을 해야한다. 상수는 let, 변수는 var 라는 키워드를 사용하여 선언한다.)

그렇다면 상수와 변수 (Constants And Variables) 을 선언하는 방법에 대해 알아보자.

# 상수 (Constant)

```
let [Name]: [Data Type] = [Value]

* example
let name: String = "VenusK"
print(name)  //VenusK

name: String = "VenusK2" //Error 발생
print(name)
```
# 변수 (Variable)
```
var [Name]: [DataType] = [Value]

* example
var name: String = "VenusK"
print(name) //VenusK

name: String ="VenusK2"
print(name) //VenusK2
```
### 상수와 변수 모두 [Data Type] 을 생략할 수 있다.
```
let [Name] = [Value]

* example 
let name = "VenusK"
```
```
var [Name] = [Value]

*example
var name = "VenusK"
```
이를 **타입 추론 (Type Inference)** 라고 하며 Value 에 따라 Swift 에서 자동으로 Data Type 을 지정해주는 기능이다. 타입 추론 (Type Inference) 은 차후에 다시 다뤄보도록 하자.

*[참조] The Swift Program Language Swift 4.1 Edition - Apple*
