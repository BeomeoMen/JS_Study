# String

JavaScript의 `String`은 텍스트 데이터를 나타내는 데 사용되는 데이터 타입이며, 문자열을 다루기 위한 다양한 기능을 제공한다.
아래에서 JavaScript의 `String` 객체에 대한 주요 특징과 사용법을 설명하겠다:

## **1. 문자열 생성:**

- 문자열은 작은 따옴표(' '), 큰 따옴표(" "), 또는 백틱(` `)으로 생성할 수 있다.

```javascript
const singleQuotedString = "Hello, world!";
const doubleQuotedString = "Hello, world!";
const backtickString = `Hello, world!`;
```

## **2. 문자열 연결:**

- `+` 연산자를 사용하여 문자열을 연결할 수 있다.

```javascript
const firstName = "John";
const lastName = "Doe";
const fullName = firstName + " " + lastName; // 'John Doe'
```

## **3. 문자열 길이:**

- `length` 프로퍼티를 사용하여 문자열의 길이를 확인할 수 있다.

```javascript
const message = "Hello, world!";
const length = message.length; // 13
```

## **4. 문자열 인덱스:**

- 문자열의 각 문자는 0부터 시작하는 인덱스를 가지며, 대괄호(`[]`)를 사용하여 특정 위치의 문자를 접근할 수 있다.

```javascript
const text = "JavaScript";
const firstChar = text[0]; // 'J'
const fifthChar = text[4]; // 'S'
```

## **5. 문자열 메서드:**

- JavaScript는 다양한 문자열 메서드를 제공하여 문자열을 조작하고 변환할 수 있다.

```javascript
const message = "Hello, world!";
const upperCase = message.toUpperCase(); // 'HELLO, WORLD!'
const lowerCase = message.toLowerCase(); // 'hello, world!'
const subString = message.substring(0, 5); // 'Hello'
const indexOfComma = message.indexOf(","); // 5
const replaced = message.replace("world", "there"); // 'Hello, there!'
```

## **6. 문자열 템플릿:**

- 백틱(` `)으로 묶인 템플릿 문자열을 사용하여 문자열 내에 변수나 표현식을 삽입할 수 있다.

```javascript
const name = "Alice";
const greeting = `Hello, ${name}!`; // 'Hello, Alice!'
```

## **7. 문자열 분할:**

- `split` 메서드를 사용하여 문자열을 특정 구분자를 기준으로 분할할 수 있다.

```javascript
const sentence = "This is a sample sentence.";
const words = sentence.split(" "); // ['This', 'is', 'a', 'sample', 'sentence.']
```

## **8. 문자열 비교:**

- 문자열을 비교할 때 `===` 또는 `!==` 연산자를 사용한다.

```javascript
const str1 = "apple";
const str2 = "banana";
const isEqual = str1 === str2; // false
```

## **9. 문자열 검색:**

- `includes`, `startsWith`, `endsWith` 메서드를 사용하여 문자열에서 특정 문자열을 검색할 수 있다.

```javascript
const text = "Hello, world!";
const includesWorld = text.includes("world"); // true
const startsWithHello = text.startsWith("Hello"); // true
const endsWithWorld = text.endsWith("world!"); // true
```

## **10. 특수 문자:** - 문자열 내에서 특수 문자를 사용하려면 역슬래시(`\`)를 사용하여 이스케이프한다.

```javascript
const message = 'He said, "Don\'t do that."';
```

## 정리

JavaScript의 String 객체는 다양한 문자열 조작 및 처리 기능을 제공하여 문자열 데이터를 효과적으로 다룰 수 있다.
이러한 기능을 통해 문자열을 다루는 다양한 작업을 수행할 수 있으며, 웹 개발, 텍스트 처리, 데이터 분석 등 다양한 응용 분야에서 사용된다.
