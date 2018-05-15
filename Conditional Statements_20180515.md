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
let stillanotherPoint = (9, 0)

switch stillAnotherPoint {
case (let distance, 0), (0, let distance)
	print("On an axis, \(distance)")
default:
	print("Not on an axis")
}
