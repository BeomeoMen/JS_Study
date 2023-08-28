# let, const 키워드와 블록 레벨 스코프

## 15.1 var 키워드로 선언한 변수의 문제점
--- 
> 변수 중복 선언 허용

- var 키워드로 선언한 변수는 중복 선언이 가능하다.
```javascript
var x = 1;
var y = 1;

// var 키워드로 선언된 변수는 같은 스코프 내에서 중복 선언을 허용
// 초기화문이 있는 변수 선언문은 자바스크립트 엔진에 의해 var 키워드가 없는 것처럼 동작
var x = 100;
// 초기화문이 없는 선언문은 무시
var y;

console.log(x); // 100
console.log(y); // 1
```

>  함수 레벨 스코프

- var 키워드로 선언한 변수는 오로지 `함수의 코드 블록만을 지역 스코프`로 인정.

```javascript
var x = 1;
if(true) {
    // x는 전역 변수다. 이미 선언된 전역 변수 x가 있으므로 x 변수는 중복 선언
    // 이는 의도치 않은 변수 재할당이 이루어짐
    var x = 10;
}
```

## 15.2 let 키워드

> 변수 중복 선언 금지

- let 키워드는 변수를 중복 선언하는 것을 허용하지 않는다.
- 변수를 중복 선언하면 문법에러(SyntaxError)가 발생

> 블록 레벨 스코프

- let 키워드로 선언한 변수는 `모든 코드 블록(함수, if, for, while, try/catch) 등을 지역 스코프를 블록 스코프`를 따른다.
```javascript
let foo = 1; // 전역 변수
{
    let foo = 2; // 지역 변수
    let bar = 3; // 지역 변수
}

console.log(foo); // 1
console.log(bar); // undefined
```

> 변수 호이스팅

- let 키워드로 선언한 변수는 "선언 단계"와 "초기화 단계"가 분리되어 진행
- 스코프의 시작 지점부터 초기화 시작 시점까지 변수를 참조할 수 없는 구간을 `일시적 사각지대`

```javascript
// 런타임 이전에 선언 단계 실행 : 아직 변수가 초기화되지 않았다.
// 초기화 이전의 일시적 사각지대에서는 변수 참조 못함
console.log(foo); // ReferenceError : foo is not defined

let foo; // 변수 선언문에서 초기화 단계 실행
console.log(foo); // undefined

foo = 1; // 할당문에서 할당
console.log(foo); // 1
```

- let 키워드로 선언한 변수는 변수 호이스팅이 발생하지 않는 것처럼 보임.
- 하지만 실제로는 호이스팅이 이루어지고 있음
- ES6에서 도입된 let, const, class를 사용한 선언문은 호이스팅이 발생하지 않는 것처럼 동작한다.

> 전역 객체와 let

- let 키워드로 선언한 전역 변수는 전역 객체(window)의 프로퍼티가 아니다.

## 15.3 const 키워드
> 선언과 초기화

- const 키워드는 `선언과 동시에 초기화`해주어야 한다.

> 재할당 금지

- var 또는 let로 선언된 변수는 재할당이 자유롭다.
- `const` 키워드로 선언한 변수는 `재할당이 금지`된다.

> 상수

- 상수는 재할당이 금지된 변수
- const 키워드로 선언된 변수에 원시 값을 할당한 경우 원시 값은 변경할 수 없는 값이고 const 키워드에 의해 재할당이 금지되므로 할당된 값을 변경할 수 있는 방법은 없다.

> const 키워드와 객체

- const 키워드로 선언된 변수에 객체를 할당한 경우 값을 변경 가능
```javascript
const person = {
    name: 'Lee'
}

// 객체는 변경 가능한 값. 따라서 재할당 없이 변경 가능
person.name = 'Kim'

console.log(perosn) // {name: 'Kim'}
```

- `const 키워는 재할당을 금지할 뿐 "불변"을 의미하지 않는다.`

## 15.6 var vs. let vs. const

- ES6를 사용한다면 var 키워드 사용안함
- 재할당이 필요한 경우 let 키워드 -> 변수의 스코프는 최대한 좁게
- const 키워드는 var, let보다 안전함





