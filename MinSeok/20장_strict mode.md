# 20장 strict mode(엄격모드)(08.31)

### strict mode(엄격모드)란?
- **암묵적 전역**
    - 자바 스크립트 엔진은 암묵적으로 전역 객체에 x 프로퍼티를 동적 생성한다.
```javascript
function foo(){
  x = 10;
}
foo();

console.log(x); // 10
```

- 하지만 개발자의 의도와 상관없이 발생한 암묵적 전역은 오류를 발생시키는 원인이 된다.
- **strict mode, ESLint**
  - 자바스크립트 언어의 `문법을 엄격히 적용`
  - `오류`를 발생할 수 있거나 `최적화 작업`에 `문제`를 일으킬 수 있는 코드에 `명시적 에러 발생`
  - ESLint는 오류의 원인을 리포팅 해주기도 한다.

### strict mode(엄격모드) 적용방법
- `전역의 선두` 또는 `몸체의 선두`에 `'use strict;'`를 추가
- 코드의 선두에 위치하지 않으면 제대로 동작 X

### 전역에 strict mode를 적용하는 것은 피하자
### 함수 단위로 strict mode를 적용하는 것도 피하자.
- strict mode는 스크립트 단위로 적용된다.
- strict mode 스크립트와 non strict mode 스크립트를 혼용하는 것은 오류 발생 유발
- 어떤 함수는 적용하고, 적용하지 않는 것은 바람직 X, 일일히 적용 불가능
- - `즉시 실행 함수`로 스크립트 전체를 감싸 `스코프를 구분`하고, 즉시 실행함수 선두에 `strict mode 적용`

### strict mode가 발생시키는 에러
1. **암묵적 전역** : 선언하지 않은 변수 참조하면 ReferenceError
2. **변수, 함수, 매개변수 삭제** : delete 연산자로 변수, 함수, 매개변수 삭제하면 SyntaxError
3. **매개변수 이름의 중복** : 중복된 매개변수 이름 사용하면 SyntaxError
4. **with문 사용** : with문 사용하면 SyntaxError

### strict mode 적용에 의한 변화
1. **일반 함수의 this** : strict mode에서 함수를 일반 함수로서 호출하면 this에 undefined가 바인딩된다.
2. **arguments 객체** : 매개변수에 전달된 인수를 재할당하여 변경해도 arguments 객체에 반영되지 않는다.