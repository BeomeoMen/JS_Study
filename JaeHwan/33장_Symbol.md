# Symbol

JavaScript의 `Symbol`은 유일하고 변경 불가능한(primitive) 데이터 타입으로, ES6(ECMAScript 2015)에서 도입되었다.
`Symbol`은 주로 객체의 프로퍼티 키로 사용되며, 특정한 목적을 가지고 있다.
아래에서 JavaScript의 `Symbol`에 대한 주요 특징과 사용법을 설명하겠다:

## **1. 유일성과 변경 불가능성**

- `Symbol`은 생성될 때마다 고유하며, 동일한 내용의 `Symbol`을 생성해도 서로 다릅니다. 따라서 `Symbol`은 유일성을 보장한다.

```javascript
const symbol1 = Symbol("apple");
const symbol2 = Symbol("apple");
console.log(symbol1 === symbol2); // false
```

- `Symbol`은 변경 불가능하므로 한 번 생성된 `Symbol`은 그 값을 변경할 수 없다.

## **2. 객체 프로퍼티 키로 사용**

- `Symbol`은 객체의 프로퍼티 키로 사용할 수 있다.
  이렇게 사용하면 다른 프로퍼티와 충돌하지 않는 고유한 키를 생성할 수 있다.

```javascript
const uniqueKey = Symbol("unique");
const obj = {
  [uniqueKey]: "This is a unique property",
};
console.log(obj[uniqueKey]); // 'This is a unique property'
```

## **3. Well-known Symbols**

- JavaScript에는 이미 정의된 몇 가지 특별한 `Symbol` 값들이 있으며, 이러한 `Symbol`들은 객체의 특수 동작을 정의할 때 사용된다.
  예를 들어 `Symbol.iterator`는 객체가 이터러블(iterable)하다는 것을 나타내는 데 사용된다.

```javascript
const iterableObject = {
  [Symbol.iterator]: function* () {
    yield 1;
    yield 2;
    yield 3;
  },
};

for (const item of iterableObject) {
  console.log(item); // 1, 2, 3
}
```

## **4. Private 프로퍼티와 메서드**

- `Symbol`을 사용하면 객체의 내부에 private한 프로퍼티와 메서드를 생성할 수 있다. 이를 통해 외부에서 접근할 수 없는 정보를 숨길 수 있다.

```javascript
const privateField = Symbol("privateField");
class MyClass {
  constructor() {
    this[privateField] = "This is a private field";
  }

  getPrivateField() {
    return this[privateField];
  }
}

const instance = new MyClass();
console.log(instance.getPrivateField()); // 'This is a private field'
console.log(instance[privateField]); // undefined (접근 불가)
```

## **5. Symbol 사용 사례**

- `Symbol`은 주로 라이브러리나 프레임워크에서 내부 구현 디테일을 숨기고 private한 키를 생성하는 데 사용된다. 또한 객체의 특수 동작을 정의할 때 유용하게 사용된다.

## 정리

`Symbol`은 객체의 프로퍼티 키로 사용되는 경우 주로 객체 내에서만 접근 가능하며, 외부에서 직접 접근할 수 없다. 이러한 특성을 통해 코드의 안정성과 보안을 향상시킬 수 있으며, 객체와 관련된 특수한 기능을 확장할 때 유용하게 사용된다.
