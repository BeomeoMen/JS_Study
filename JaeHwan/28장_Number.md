# Number

JavaScript의 Number는 숫자 데이터 유형을 나타내는 기본 데이터 유형 중 하나이다.
Number는 정수와 부동 소수점 숫자를 모두 표현할 수 있으며, 숫자와 관련된 다양한 작업을 수행하는 데 사용된다.
다음은 Number에 대한 주요 특징과 사용법에 대한 설명이다

## 정수 및 부동 소수점 숫자

Number는 정수와 부동 소수점 숫자를 모두 표현할 수 있다.
예를 들어, 42나 3.14와 같은 값을 나타낼 수 있다.

```javascript
const integer = 42;
const floatingPoint = 3.14;
```

## 산술 연산

Number는 산술 연산에 사용된다.
기본적인 산술 연산자(덧셈, 뺄셈, 곱셈, 나눗셈 등)를 사용하여 숫자를 조작할 수 있다.

```javascript

const a = 10;
const b = 5;
const sum = a + b; // 덧셈
const difference = a - b; // 뺄셈
const product = a \* b; // 곱셈
const quotient = a / b; // 나눗셈
```

## NaN (Not-a-Number)

JavaScript의 Number에는 NaN이라는 특수한 값이 있다.
이 값은 "숫자가 아님"을 나타내며, 잘못된 산술 연산의 결과로 반환될 수 있다.

```javascript
const result = 10 / "apple"; // NaN
```

## Infinity

Number는 무한대(Infinity)를 나타내는데 사용된다.
이 값은 양의 무한대(Infinity)와 음의 무한대(-Infinity)로 나뉜다.

```javascript
const positiveInfinity = Infinity;
const negativeInfinity = -Infinity;
```

## 다양한 메서드

Number 객체는 여러 유용한 메서드를 제공한다.
예를 들어, 숫자를 반올림하거나 고정 소수점 형식으로 문자열로 변환하는 등의 작업을 수행할 수 있다.

```javascript
const num = 3.14159;
const roundedNum = num.toFixed(2); // "3.14"
```

## Number 객체 vs. 리터럴:

Number 객체와 숫자 리터럴(예: 42 또는 3.14)은 유사하지만 몇 가지 차이가 있다.
Number 객체는 Number() 생성자를 사용하여 생성하며, 일반적으로 리터럴 표기법을 사용하는 것이 권장된다.

```javascript
const numLiteral = 42;
const numObject = new Number(42);
```

## NaN 확인

NaN 값을 확인할 때 isNaN() 함수를 사용하면 된다.

```javascript
const result = 10 / "apple";
if (isNaN(result)) {
  console.log("It's NaN!");
}
```

JavaScript의 Number는 다양한 수학 및 계산 작업을 수행하는 데 필수적인 데이터 유형이며, 주로 웹 개발 및 데이터 처리에 사용된다.
