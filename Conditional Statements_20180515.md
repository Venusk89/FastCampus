## If Statement

### if

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



