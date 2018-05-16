## If Statement

### if
`if` Basic Syntax

`condition` 의 `Bool` 값이 참일 경우 `code` 실행.

```
if condition {
	code
}
```
### if - else

`condition`의 `Bool` 값이 참일 경우 `if` 문 `code` 실행.

`condition`의 `Bool` 값이 거짓일 경우 `else` 문 `code` 실행.

```
if condition {
	code
} else {
	code
}
```

### if - else if

`if`문 `condition`의 `Bool` 값이 참일 경우 `if` 문 `code` 실행.

`if`문 `condition`의 `Bool` 값이 거짓일 경우 `else if` 문으로 이동.

`else if`문 `condition` 의 `Bool` 값이 참일 경우 `else if` 문 `code` 실행.

```
if condition {
	code
} else if condition {
	code
}
```

### if - else if - else

`if` 문 `condition`의 `Bool` 값이 참일 경우 `if` 문 `code` 실행.

`if` 문 `condition`의 `Bool` 값이 거짓일 경우 `else if` 문으로 이동.

`else if`문 `condition`의 `Bool` 값이 참일 경우 `else if` 문 `code` 실행.

`else if`문 `condition`의 `Bool` 값이 거짓일 경우 `else` 문 `code` 실행.

```
if condition {
	code
} else if condition {
	code
} else {
	code
}
```

>`if - if` 문과 `if - else if` 문의 차이점
>
>```
>var temperatureInFahrenheit: Int = 72
>
>if temperatureInFahrenheit <= 32 {
>	print("It's very cold")
>}
>if temperatureInFahrenheit >= 86 {
>	print("It's really warm")
>}
>```
>
>```
>var temperatureInFahrenheit: Int = 72
>
>if temperatureInFahrenheit <= 32 {
>	print("It's very cold")
>} else if temperatureInFahrenheit >= 86 {
>	print("It's really warm")
>}
>```
>
>*`if - if` 문의 경우 첫번째 `if` 의 `Bool` 값이 `true` 여도 다음 `if` 가 실행된다.*
>
>*`if - else if` 문의 경우 첫번째 `if` 의 `Bool` 값이 `true` 라면 `else if`가 실행되지 않는다.*

### if Logical Operator

`if`문의 AND 연산자

```
if (a > 0) && (b % 2 == 0){

}
```

```
if a > 0, b % 2 == 0 {

}
```

`if`문의 OR 연산자

```
if (a > 0) || (b % 2 == 0) {

}
```

## Switch Statements

`switch` Basic Syntax

`switch` 의 `value` 값에 따라 `case` 및 `default` 의 `code` 가 실행된다.

```
switch value {
case pattern:
	code
default:
	code
}
```
> *`switch` 문은 반드시 모든 사례를 반드시 다루어야 한다.*
> 
> *`case` 로 모두 충족할 수 없을 경우에는 `default` 로 처리해 주어야 한다.*
> 
> *`case` 및 `default` 내에는 어떤 형태로든 `code`가 들어가야 한다*

`switch` 문을 `if` 문으로 변경할 수 있다.

```
let alphabet: Character = "a"

switch alphabet {
case "a":
	print("The first letter of alphabet")
case "z":
	print("The last letter of alphabet")
default:
	break
}
```
```
let alphabet: Character = "a"

if alphabet == "a"
	print("The first letter of alphabet")
} else if alphabet == "z"
	print("The last letter of alphabet")
} else {

}
```

### Interver Matching

범위 조건에 대한 `switch`문을 작성할 수 있다.

```
let apporoximateCount = 30

switch approximateCount {
case 0...50:
	print("0 ~ 50")
case 51...100:
	print("51 ~ 100")
default:
	print("Something else")
}
```

### Compound case

하나의 `case` 에 여러가지 조건을 넣을 수 있다.

```
let someCharacter {
case "a", "e", "i", "o", "u":
	print("\(someCharacter) is vowel.")
case "b", "c", "d", "f", "g", "h", "j", "k", "l", "m", "n",
     "p", "q", "r", "s", "t", "v", "w", "x", "y", "z":
	print("\(someCharacter) is consonant")
default:
	priunt("\(someCharacter) is not a vower or a consonant")
```
> *`case` 문의 , 은 OR 의 기능을 한다.*

### Value binding

```
let stillAnotherPoint = (9, 0)

switch stillAnotherPoint {
case (let distance, 0), (0, let distance)
	print("On an axis, \(distance) from the origin")
default:
	print("Not on an axis")
}
```
`let distance`와 같이 변수와 상수를 이용해 Data 를 전달할 수 있다.

Value binding 을 사용하지 않고 작성하면 아래와 같다.

```
swtich stillAnotherPoint
case (9, 0):
	print("On an axis, 9 from the origin)
case (0, 9):
	print("On an axis, 9 from the origin)
default:
	print("Not on an axis")
}
```

### No default case
`case` 에서 모든 경우의 수를 다루었을 경우에는 `default` 를 사용하지 않아도 된다.

```
let c = true

switch c {
case ture:
	print("true)
case false:
	print(:false)
}
```
`c` 의 Data Type 은 `true` 와 `false` 만 존재하는 `Bool` 이므로 `case` 에서 모든 경우의 수를 다루었다.

### Fallthrough

`switch` 문의 `value` 값에 해당하는 `case` 를 실행한 뒤 `break` 를 하지 않고 다음 `case` 를 실행한다.
> 다른 언어에서는 `switch` 문에서 `fallthrough` 가 기본이지만 Swift 에서는 `break` 가 기본이며, `fallthrough` 가 옵션이다.

```
let integerToDescribe = 5
var description = "The number \(integerToDescribe) is"

switch integerToDescribe {
case = 2, 3, 5, 7, 11, 13, 17, 19:
	desciption += " a prime number, and also"
	fallthrough
default:
	description += " an integer."
}
```

## Early Exit

### Guard Statement

`gaurd` Basic Syntax

```
guard condition else {
	code
}
```
`guard`문은 `if` 과 마찬가지로 `condition` 의 `Bool` 의 `Value` 로 동작을 한다.

`guard`문 `condition` 의 `Value` 가 거짓 이라면 `else` 내부의 코드를 실행하게 되며, `else` 내부에는 상위의 코드를 종료하는 `code` 를 포함하게 된다.

>`if`문과 `guard` 문의 비교
>
>```
>for i in 0...3 {           |      for i in 0...3 {
>	if i == 2 {              |  	     guard i == 2 else {
>		print(i)           |		continue
>	} else {                 |		}
>		continue           |  	     print(i)
>	}                        |       }    
>}                          |
>```


