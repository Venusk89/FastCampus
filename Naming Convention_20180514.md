Program Coding 작업을 하다보면, 어떠한 Type 의 이름을 정하는 것이 굉장히 어려운 일이라고 깨닫게 될 것이다.
(개발자들이 가장 어려워 하는 것 중 하나가 이름 짓기라는 말도 있지 않는가)

Apple 에서 권장하는 Naming Convention 은 다음과 같다.

### Pascal Case
 + 첫 스펠과 다음에 오는 단어의 첫 스펠을 대문자로 작성하는 방법.
 + Filename, Class, Structure, enum, protocol 등 구조체에 사용한다.
 
 > *example) FisrtClass
 

### Carmel Case
 + 첫 스펠을 소문자로, 다음에 오는 단어의 첫 스펠은 대문자로 작성하는 방법.
 + 구조체를 제외한 대부분의 이름에 사용한다.

> *example) aMultipleOfTwo, drawingSketch

### 앞에서 사용한 Naming 은 사용할 수 없다.

### 기본적으로 Apple 에서 제공하는 Keyword 는 사용할 수 없으나, backquote ( ' ) 를 이용하면 사용이 가능하다
> *example) 'let' 'var' 'class'

### 다음과 같은 경우도 사용이 불가능하다.
 + 같은 스코프 범위내에서 중복된 이름.
 + 공백문자
 + 수학 기호
 + 화살표
 + 숫자로 시작하는 이름
