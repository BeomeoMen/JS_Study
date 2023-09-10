# Set과 Map

- Set 객체는 중복되지 않는 유일한 값들의 집합이다.

<br>
<br>
<br>

> Set 객체는 배열과 유사하지만 다음과 같은 차이가 있다.

| 구분                                 | 배열 | Set 객체 |
| ------------------------------------ | ---- | -------- |
| 동일한 값을 중복하여 포함할 수 있다. | O    | X        |
| 요소 순서에 의미가 있다.             | O    | X        |
| 인덱스로 요소에 접근할 수 있다.      | O    | X        |

<br>

- Set 객체는 Set 생성자 함수로 생성하고, 이터러블을 인수로 전달받아 Set 객체를 생성한다. 이때 이터러블의 중복된 값을 Set 객체에 요소에 저장되지 않는다.

```js
const set = new Set();
console.log(set); // Set(0) {}
```

## 메서드

Set 객체의 요수 개수 -> `Set.prototype.size` 프로퍼티를 사용

Set 객체의 요수 추가 -> `Set.prototype.add` 메서드를 사용

Set 객체의 요수 존재 여부 확인 -> `Set.prototype.has` 메서드를 사용

Set 객체의 요수 삭제 -> `Set.prototype.delete` 메서드를 사용

Set 객체의 요수 일괄 삭제 -> `Set.prototype.clear` 메서드를 사용

Set 객체의 요수 순회 -> `Set.prototype.forEach` 메서드를 사용

교집합 -> `Set.prototype.intersection` 메서드를 사용

합집합 -> `Set.prototype.union` 메서드를 사용

차집합 -> `Set.prototype.difference` 메서드를 사용

부분집합과 상위 집합 -> `Set.prototype.isSuperset` 메서드를 사용
