# 모딥다 스터디 #1


주제: 04장 변수, 06장 데이터 타입

# 04장 변수

## 4.1 변수란?

- 컴퓨터는 **CPU**를 사용해 연산하고, **메모리**를 사용해 데이터를 기억한다.
- 메모리는 데이터를 저장할 수 있는 **메모리 셀(memory cell)**의 집합체다. 메모리 셀 하나의 크기는 **1바이트(=8비트)**이다.
- 컴퓨터는 메모리 셀의 크기(1 byte)로 데이터를 저장(write)하거나 읽어들인다.
- 각 메모리 셀은 고유의 **메모리 주소**를 갖는다. 메모리 주소는 메모리 공간의 위치를 나타내며, 0부터 시작해서 메모리의 크기(총 byte 수)만큼 정수로 표현된다.
- **컴퓨터의 단위**
    
    ```jsx
    1 byte = 8 bit
    1 KB = 1,024 byte = 2^10 byte
    1 MB = 1,024 KB = 2^20 byte
    1 GB = 1,024 MB = 2^30 byte
    1 TB = 1,024 GB = 2^40 byte
    ```
    
- **리터럴(literal)**은 소스 코드 상에서 직접 작성된 값을 의미한다. 즉, 코드에 있는 값을 그대로 나타내는 것이다. 예를 들어, 숫자, 문자열, 불리언, 객체, 배열 등의 값을 직접 작성하여 변수나 상수에 할당하는 것이 리터럴이다.
    
    ```jsx
    let x = 5; // 5는 숫자형 리터럴입니다.
    let message = "Hello, world!"; // "Hello, world!"는 문자열 리터럴입니다.
    ```
    

## 4.2 식별자

- **식별자**는 값이 아니라 **메모리 주소를 기억**하고 있다. 즉, 메모리 주소에 붙인 이름.
식별자는 **변수 이름**만 의미하는 게 아니고 **함수, 클래스 등의 이름**이 모두 식별자다.

## 4.3 변수 선언

- **var** 키워드의 단점: 의도치 않게 **전역 변수가 선언**될 수 있다.
- **ES6은 ES5의 상위 집합**으로, ES6은 기본적으로  하위 호환성을 유지하면서 ES5의 기반 위에 새로운 기능을 추가한 것이다.

**변수 선언** 

변수를 정의하는 것을 의미한다. var , let , const 키워드 사용(ES6 에서 let 과 const 추가)

```jsx
var developer;
```

**변수 할당** 

변수가 선언된 후 대입 연산자(=)를 통해 값을 넣어주는 것을 의미한다

```jsx
var developer;
developer = 'espania';
```

**변수 초기화** 

변수를 선언함과 동시에 값을 넣어 주는 것을 의미한다.

```jsx
var developer = 'espania';
```

## 4.4 호이스팅

- **변수 호이스팅(variable hoisting):** 변수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 **자바스크립트 고유의 특징.**
변수 선언(선언 단계와 초기화 단계)이 소스코드가 순차적으로 실행되는 런타임 이전 단계에서 먼저 실행된다.

## 4.5 값의 할당

- 자바스크립트 엔진은 변수의 선언과 값의 할당을 2개의 문으로 나누어 각각 실행한다.
※ 주의할 점으로 변수에 값을 할당할 때는 이전 값 undefined가 저장되어 있던 메모리 공간을 지우고 그 메모리 공간에 할당 값 80을 저장하는 것이 아니라 **새로운 메모리 공간을 확보하고 그곳에 할당 값 80을 저장한다**는 점이다.

## 4.6 값의 재할당

- 값을 재할당할 수 없어서 변수에 저장된 값을 변경할 수 없다면 변수가 아니라 **상수**라 한다.
(예) **const** 키워드를 사용해 선언한 변수 (단, const 키워드가 반드시 상수만을 위해 사용하지는 않는다는 점 알아두기)

## 4.7 식별자 네이밍 규칙

- 문자 , 숫자 , _ , $ 포함 가능
단, 숫자로는 시작하지 못하고 예약어는 식별자로 사용 불가.
(예) case, class, default, delete, new, … 등은 예약어
(예) var first-name 등은 ‘-’가 포함되어 사용 불가
- 대소문자 구분됨.
(예) var firstname과 var Firstname은 서로 다른 변수
- 네이밍 컨벤션(naming convention)
JS에서는 카멜 케이스와 파스칼 케이스를 사용함.

# SeoYoung

## Intro. 컴퓨터 구조 이해

- 메모리memory란

  > 데이터가 메모리 상의 임의의 위치(메모리 주소)에 기억(저장)되면 CPU가 이를 읽어들이고 연산을 수행하는 방식

  메모리란 데이터를 저장할 수 있는 메모리 셀의 집합체다.

  ![IMG_0397.jpg](%E1%84%86%E1%85%A9%E1%84%83%E1%85%B5%E1%86%B8%E1%84%83%E1%85%A1%20Week1%2063fb1f0368bc442fbad26736ed86688f/IMG_0397.jpg)

  메모리 셀 하나의 크기는 1바이트(8비트)이며, 컴퓨터는 메모리 셀의 크기, 즉 1바이트 단위로 데이터를 저장하거나 읽어 들인다.

  각 셀은 메모리 주소를 갖는다. 메모리 주소는 메모리 공간의 위치를 나타내며, 메모리에 저장되는 데이터는 데이터의 종류(숫자, 텍스트, 이미지, 동영상 등)와 상관없이 모두 2진수로 저장된다.

  ![IMG_0398.jpg](%E1%84%86%E1%85%A9%E1%84%83%E1%85%B5%E1%86%B8%E1%84%83%E1%85%A1%20Week1%2063fb1f0368bc442fbad26736ed86688f/IMG_0398.jpg)

  예제 숫자 10과 20이 있다. 둘은 메모리 상의 임의의 위치(메모리 주소)에 기억(저장)되고, CPU는 이 값을 읽어들여 연산을 수행한다. 연산 결과로 생성된 숫자 값 30도 메모리 상의 임의의 위치에 저장된다.

- 값을 재사용하기 위한 식별자, 변수variable

  > 변수는 값의 위치를 가리키는 상징적인 이름

  ![IMG_0399.jpg](%E1%84%86%E1%85%A9%E1%84%83%E1%85%B5%E1%86%B8%E1%84%83%E1%85%A1%20Week1%2063fb1f0368bc442fbad26736ed86688f/IMG_0399.jpg)

  CPU가 연산을 수행한 값을 재사용하려고 한다면, 메모리 주소를 통해 값에 직접 접근하는 방법은 옳지 않다. 이때 나오는 개념이 변수다.

  변수는 하나의 값을 저장하기 위해 확보한 메모리 공간 자체 또는 그 메모리 공간을 식별하기 위해 붙인 이름을 말한다. 

  변수 이름을 식별자idenrifier라고도 한다. 식별자는 어떤 값을 구별해서 식별할 수 있는 고유한 이름을 말한다. 메모리 주소에 붙인 이름이라고 할 수 있다.

  식별자는 값이 아니라 메모리 주소를 기억하고 있다. 식별자로 값을 구별해서 식별한다는 것은 식별자가 기억하고 있는 메모리 주소를 통해 메모리 공간에 저장된 값에 접근할 수 있다는 의미다.

- 변수를 사용하려면 반드시 선언이 필요하다

  > 식별자는 메모리 주소에 붙인 이름이라고 할 수 있다

  값을 저장하기 위한 메모리 공간을 확보하고 변수 이름과 확보된 메모리 공간의 주소를 연결해서 값을 저장할 수 있게 준비하는 것이다.

  변수를 사용하려면 반드시 선언이 필요하고, `var` `let` `const` 키워드를 사용한다.

## 변수 선언

---

> - 선언 단계 : 변수 이름을 등록해서 자바스크립트 엔진에 변수의 존재를 알린다.

- 초기화 단계 : 값을 저장하기 위한 메모리 공간을 확보하고 암묵적으로 `undefined`를 할당해 초기화한다.

> 

### 변수 선언과 값의 할당

`var` 키워드를 만나면 자바스크립트 엔진은 뒤에 오는 변수 이름으로 새로운 변수를 선언한다.

```jsx
var score;
```

다음과 같이 변수 이름을 등록하고 값을 저장할 메모리 공간을 확보한다.

값을 아직 할당하지 않았으므로 확보된 메모리 공간에는 `undefined` 라는 값이 할당되어 초기화된다.

### 값의 재할당

자바스크립트 엔진은 변수의 선언과 값의 할당을 2개의 문으로 나누어 실행된다. 따라서 변수에 `undefined`가 할당되어 초기화되는 것은 변함이 없다.

변수에 값을 할당할 때는 이전 값이 저장되어 있던 메모리 공간을 지우고 그 메모리 공간에 할당 값을 새롭게 저장하는 것이 아니라, 새로운 메모리 공간을 확보하고 그곳에 저장한다는 점에 유의하자.

```jsx
console.log(score);
//222:1 Uncaught ReferenceError: score is not defined
//    at <anonymous>:1:13
//(
score = 80; // 값의 재할당
// 80
var score;
// undefined
console.log(score);
// 80
// undefined
```

# 06장 데이터 종류

## 6.1 숫자 타입

- 정수나 실수 타입이 따로 없고 하나의 숫자 타입만 존재한다.
모든 수를 **실수**로, **10진수**로 취급한다.
- 독특하게 **Infinity, -Infinity, NaN** 값을 표현할 수 있다.

## 6.2 문자열 타입

- UTF-16의 집합. 전 세계 대부분의 문자를 표현할 수 있다.

## 6.3 템플릿 리터럴

템플릿 리터럴이란 문자열 표기법으로 편리한 문자열 처리 기능을 제공한다. **`을 사용?**

- **멀티라인 문자열(multi-line string)**
- **표현식 삽입(expression literal)**
문자열은 **문자열 연산자 +**를 사용해 연결할 수 있다. +연산자는 피연산자 중 하나 이상이 문자 열인 경우 문자열 연결 연산자로 동작한다. 그 외의 경우는 **덧셈 연산자**로 동작한다.
    
    표현식을 삽입하려면 **${}**으로 표현식을 감싼다. 이 때 표현식의 평가 결과가 문자열이 아니더라도 **문자열로 타입**이 강제로 **변환**되어 삽입된다.
    
- **태그드 템플릿(tagged template)**

## 6.5 undefined 타입

- 개발자가 의도적으로 할당하기 위한 값 X
- 자바스크립트 엔진이 변수를 초기화할 때 사용하는 값 O
- 변수에 값이 없다는 것을 명시하고 싶을 때는? null을 할당

## 6.6 null 타입

- 변수에 null을 할당하는 것은 변수가 이전에 참조하던 값을 더 이상 참조하지 않겠다는 의미다.
자바스크립트 엔진은 누구도 참조하지 않는 메모리 공간에 대해 가비지 콜렉션을 수행할 것이다.
- document.querySelector 메서드는 조건에 부합하는 HTML 요소를 검색할 수 없는 경우에 에러 대신 null을 반환한다.

## 6.9 데이터 타입

데이터 타입이 필요한 이유?

- 값을 저장할 때 확보해야 하는 메모리 공간의 크기를 결정
- 값을 참조할 때 한 번에 읽어 들여야 할 메모리 공간의 크기를 결정
- 메모리에서 읽어들인 2진수를 어떻게 해석할지 결정

## 6.10 동적 타이핑

- C, C++, 자바, 코틀린 등은 정적 타입 언어이다. 변수 선언 시점에 변수의 타입이 결정된다.
- 자바스크립트는 정적 타입 언어와 다르게 변수를 선언할 때 타입을 선언하지 않는다. 단지 var, let, const 키워드를 사용해 변수를 선언할 뿐이다. 자바스크립트에의 변수에는 어떤 데이터 타입의 값이라도 자유롭게 할당할 수 있다.
- 정적 타입 언어는 변수 **선언 시점**에 변수의 타입이 결정되고 변수의 타입을 변경할 수 없다. 자바스크립트에서는 값을 **할당하는 시점**에 변수의 타입이 동적으로 결정되고 변수의 타입을 언제든지 자유롭게 변경할 수 있다. 이러한 자바스크립트의 특징을 **동적 타이핑**이라고 한다.

## 에러의 종류

- **ReferenceError (참조 에러)**
    
    식별자를 통해 값을 참조하려 했지만 자바스크립트 엔진이 등록된 식별자를 찾을 수 없을 때 발생하는 에러. 모든 식별자는 사용하려면 반드시 선언이 필요하다.
    

## 질문

- 직접적인 **메모리 제어**를 허용하는 프로그래밍 언어가 있는가?
    
    일반적으로 메모리를 직접적으로 조작하는 것은 위험하며, 대부분의 프로그래밍 언어에서는 메모리를 관리하기 위한 추상화된 기능을 제공한다. 하지만 **C나 C++** 같은 저수준 언어에서는 **포인터**를 사용하여 메모리 주소를 직접 조작할 수 있다.
    
- **p.45 예제 04-10 이유에 대해 얘기해보기.**
    
    변수를 사용하려면 선언이 필요하다. 선언하지 않고 식별자에 접근하면 ReferenceError 발생한다. 이는 런타임 단계이고, 따라서 런타임 단계 이전에 변수가 먼저 초기화 된 뒤 첫 번째 console.log를 지나 undefined이 표시된다. 그 뒤에 score=80;으로 값이 할당되어 두 번째 console.log를 지날 땐 80가 표시된다.
    
    ```jsx
    console.log(score);
    
    score=80;
    var score;
    
    console.log(score);
    ```
    
- JS에서 **토큰**이란?
    
    JavaScript에서 토큰(token)은 소스 코드를 구성하는 최소한의 구성 요소이다.  JavaScript 코드는 토큰으로 분할되고 이들은 문법 구조의 구성 요소인 구문으로 조합된다.
    
    예를 들어, 변수를 선언하고 값을 할당하는 코드를 생각해보면, 변수 이름과 할당 연산자, 그리고 값의 데이터 유형에 해당하는 토큰으로 구성됩니다. 다음은 이 코드를 구성하는 토큰의 예이다.
    
    ```jsx
    var x = 10;
    // "var", "x", "=", "10", ";" 은 토큰입니다.
    ```
    
# SeoYoung

6-9. 데이터 타입의 필요성?

### 데이터 타입에 의한 값의 해석

> - 값을 저장할 때 확보해야 하는 **메모리 공간의 크기** 결정

- 값을 참조할 때 한 번에 읽어 들어야 할 **메모리 공간의 크기** 결정
- 메모리에서 읽어 들인 2**진수를 어떻게 해석**할지 결정

> 

자바스크립트 엔진은 데이터 타입, 즉 값의 종류에 따라 정해진 크기의 메모리 공간을 확보한다. 즉, 변수에 할당되는 값의 데이터 타입에 따라 확보해야 할 메모리 공간의 크기가 결정된다.

`score` 변수 예시를 들면, 변수에 숫자 타입에 값이 할당되어 있으므로 자바스크립트 엔진은 `score`  변수를 숫자 타입으로 인식한다. 숫자 타입은 8바이트 단위로 저장되므로 `score` 변수를 참조하면 8바이트 단위로 메모리 공간에 저장된 값을 읽어 들인다.

<aside>
🗣️ 심벌 테이블 ?
컴파일러 또는 인터프리터는 심벌 테이블이라고 하는 자료구조를 통해 
식별자를 키로 바인딩된 값의 메모리 주소, 데이터 타입, 스코프 등을 관리한다.


</aside>

`score` 변수를 참조하여 메모리 공간의 주소에서 읽어 들인 2진수를 숫자로 해석한다. 

### 동적 타이핑

자바스크립트 모든 값은 데이터 타입을 갖는데, 변수는 데이터 타입을 가질까?

자바스크립트는 정적 타입 언어(C, C++, 자바, 코틀린 등)와 다르게 변수를 선언할 때 타입을 선언하지 않는다. 다만 `var` , `let` , `const`  키워드를 사용해 변수를 선언할 뿐이다. 자바스크립트 변수는 미리 선언한 데이터 타입의 값만 할당할 수 있는 것이 아니다.

즉, 자바스크립트의 변수는 선언이 아닌 할당에 의해 타입이 결정된다. 재할당에 의해 변수의 타입은 언제든지 동적으로 변할 수 있다.