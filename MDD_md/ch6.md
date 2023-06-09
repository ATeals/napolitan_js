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

  score = 80;
  var score;

  console.log(score);
  ```
- JS에서 **토큰**이란?
  JavaScript에서 토큰(token)은 소스 코드를 구성하는 최소한의 구성 요소이다. JavaScript 코드는 토큰으로 분할되고 이들은 문법 구조의 구성 요소인 구문으로 조합된다.
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

`score` 변수 예시를 들면, 변수에 숫자 타입에 값이 할당되어 있으므로 자바스크립트 엔진은 `score` 변수를 숫자 타입으로 인식한다. 숫자 타입은 8바이트 단위로 저장되므로 `score` 변수를 참조하면 8바이트 단위로 메모리 공간에 저장된 값을 읽어 들인다.

<aside>
🗣️ 심벌 테이블 ?
컴파일러 또는 인터프리터는 심벌 테이블이라고 하는 자료구조를 통해 
식별자를 키로 바인딩된 값의 메모리 주소, 데이터 타입, 스코프 등을 관리한다.

</aside>

`score` 변수를 참조하여 메모리 공간의 주소에서 읽어 들인 2진수를 숫자로 해석한다.

### 동적 타이핑

자바스크립트 모든 값은 데이터 타입을 갖는데, 변수는 데이터 타입을 가질까?

자바스크립트는 정적 타입 언어(C, C++, 자바, 코틀린 등)와 다르게 변수를 선언할 때 타입을 선언하지 않는다. 다만 `var` , `let` , `const` 키워드를 사용해 변수를 선언할 뿐이다. 자바스크립트 변수는 미리 선언한 데이터 타입의 값만 할당할 수 있는 것이 아니다.

즉, 자바스크립트의 변수는 선언이 아닌 할당에 의해 타입이 결정된다. 재할당에 의해 변수의 타입은 언제든지 동적으로 변할 수 있다.
