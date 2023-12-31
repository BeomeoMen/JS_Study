# 7번째 데이터 타입 Symbol

## 심벌이란?

- 변경 불가능한 원시 타입의 값
- 다른 값과 중복되지 않는 유일무이한 값

## 심벌 값의 생성

> Symbol 함수

- 다른 값과 절대 중복되지 않는 유일무이한 값
- new 연산자와 함께 호출하지 않는다.

> Symbol.for/Symbol.keyFor 메서드

- Symbol.for 메서드는 인수로 전달받은 문자열을 키로 사용하여 키와 심벌 값의 쌍들이 저장되어 있는 전역 심볼 레지스트리에서 해당 키와 일치하는 심벌 값을 검색
  - 검색에 성공하면 새로운 심벌 값을 생성하지 않고 검색된 심벌 값을 반환
  - 검색에 실패하면 새로운 심벌 값을 생성하여 Symbol.for 메서드의 인수로 전달된 키로 전역 심벌 레지스트리에 저장한 후, 생성된 심벌 값을 반환

```js
// 새로운 심벌 값 생성
const s1 = Symbol.for('mySymbol');
// 해당 심벌 값 반환
const s2 = Symbol.for('mySymbol');

console.log(s1 === s2); // true
```

- Symbol.keyFor는 전역 심벌 레지스트리에 저장된 심벌 값의 키를 추출

## 심벌과 상수

- 값에는 특별한 의미가 없고 상수 이름 자체에 의미가 있는 경우
- 무의미한 상수 대신 중복될 가능성이 없는 유일무이한 심벌 값을 사용

### 심벌은 하위 호환성을 보장하기 위해 도입되었다.
