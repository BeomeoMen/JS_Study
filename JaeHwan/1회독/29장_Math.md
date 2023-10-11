# Math

JavaScript의 `Math` 객체는 수학적인 연산을 수행하기 위한 여러 메서드와 상수를 제공하는 내장 객체이다.
`Math` 객체를 사용하면 다양한 수학적 작업을 쉽게 수행할 수 있다.
다음은 몇 가지 `Math` 객체의 주요 메서드와 상수에 대한 설명이다:

## **1. 수학적 상수**

- `Math.PI`: 원주율 (π) 상수를 반환한다.
- `Math.E`: 자연 로그의 밑인 오일러 상수를 반환한다.

```javascript
const pi = Math.PI; // 3.141592653589793
const euler = Math.E; // 2.718281828459045
```

## **2. 기본 연산 메서드**

- `Math.abs(x)`: 숫자 `x`의 절댓값을 반환한다.
- `Math.round(x)`: 가장 가까운 정수로 반올림한 값을 반환한다.
- `Math.ceil(x)`: 숫자 `x`를 올림한 정수를 반환한다.
- `Math.floor(x)`: 숫자 `x`를 내림한 정수를 반환한다.
- `Math.max(x1, x2, ... , xn)`: 주어진 숫자 중 가장 큰 값을 반환한다.
- `Math.min(x1, x2, ... , xn)`: 주어진 숫자 중 가장 작은 값을 반환한다.

```javascript
const absoluteValue = Math.abs(-5); // 5
const roundedValue = Math.round(3.7); // 4
const ceilingValue = Math.ceil(4.1); // 5
const floorValue = Math.floor(4.9); // 4
const maxValue = Math.max(1, 3, 2, 5); // 5
const minValue = Math.min(1, 3, 2, 5); // 1
```

## **3. 거듭제곱 및 제곱근**

- `Math.pow(x, y)`: `x`의 `y` 제곱을 반환한다.
- `Math.sqrt(x)`: 숫자 `x`의 제곱근을 반환한다.

```javascript
const powerResult = Math.pow(2, 3); // 8 (2^3)
const sqrtResult = Math.sqrt(25); // 5 (√25)
```

## **4. 삼각 함수**

- `Math.sin(x)`: 사인 함수를 계산하여 반환한다.
- `Math.cos(x)`: 코사인 함수를 계산하여 반환한다.
- `Math.tan(x)`: 탄젠트 함수를 계산하여 반환한다.

```javascript
const sineValue = Math.sin(Math.PI / 2); // 1 (sin(π/2) = 1)
const cosineValue = Math.cos(Math.PI); // -1 (cos(π) = -1)
const tangentValue = Math.tan(Math.PI / 4); // 1 (tan(π/4) = 1)
```

## **5. 난수 생성**

- `Math.random()`: 0 (포함)에서 1 (미포함) 사이의 난수를 반환한다.

```javascript
const randomValue = Math.random(); // 0 이상 1 미만의 난수
```

## **6. 로그 함수**

- `Math.log(x)`: 자연 로그 (밑이 `Math.E`)를 반환한다.
- `Math.log10(x)`: 10을 밑으로 하는 로그 값을 반환한다.

```javascript
const naturalLog = Math.log(Math.E); // 1 (ln(e) = 1)
const logBase10 = Math.log10(100); // 2 (log10(100) = 2)
```

## **7. 각종 상수**

- `Math.LN2`: 2의 자연 로그 값 (ln(2))을 반환한다.
- `Math.LN10`: 10의 자연 로그 값 (ln(10))을 반환한다.

```javascript
const ln2Value = Math.LN2; // 0.6931471805599453
const ln10Value = Math.LN10; // 2.302585092994046
```

`Math` 객체는 JavaScript에서 수학적 계산을 수행하는 데 필요한 다양한 도구를 제공하며, 웹 개발, 데이터 분석 및 과학적 계산과 같은 다양한 응용 프로그램에서 유용하게 사용된다.
