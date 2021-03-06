타입 선언 (Type Annotation) 은 변수 선언시 Data Type 을 명확하게 지정해 주는 것이다.

```
let year: Int = 2018

let language: String
language = "Swift" 
//let 은 상수 (Constants) 로서 선언을 한 뒤 값 (Value) 을 변경 할 수 없지만 초기값을 지정해 주지 않으면 이후에 값을 변경 할 수 있다.
```

```
var red, green, blue : Double
red = 255.0
green = 3.14
blue = 2031.12930 //한 줄에 여러개의 상수 (Constants) 및 변수 (Variables) 의 Data Type 을 지정할 수 있다.
```
타입추론 (Type Inference) 은 Swift 에서 지원하는 기능이다.

The Swift Programming Language (Swift 4.1) - Apple 에 따르면 타입추론 (Type Inference) 을 다음과 같이 설명하고 있다.

*‘Swift can almost always infer the type to be used for that constant or variable, as described in Type Safety and Type Inference.'*

간단하게 해석하자면, '스위프트는 항상 Type Safety 와 Type Inference 에 서술된 것에 따라 상수와 변수 타입을 추론한다.' 라고 서술되어 있다. 

아래의 예를 살펴보자.

```
var name: String = "VenusK"
print(type(of: name)) //String

var name2 = "VenusK"
print(type(of: name2)) //String
```
```
var age: Int = 20
print(type(of: age)) //Int
var age2 = 20
print(type(of: age2)) //Int
```
위와 같이 Data Type 을 생략해도 Swift 의 Type Inference 기능을 통해 자동으로 Data Type 이 지정된다.

보는 바와 같이 타입추론 (Type Inference) 은 매우 편리한 기능이지만
자칫 잘못된 타입추론 (Type Inference) 로 인해 오류가 생기면 이 오류를 찾는 것이 상당히 번거로울 수 있다.
그래서 Swift 를 처음 시작하는 사람이라면, 타입추론 (Type Inference) 보다는 Data Type 을 입력해 주는 것을 권장한다.



*[참조] The Swift Programming Language (Swift 4.1 Edition) - Apple*
