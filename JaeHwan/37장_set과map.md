# set과 map

Set과 Map은 JavaScript의 데이터 구조로, 각각 고유한 특징과 용도를 가지고 있다.

## **Set**

Set은 중복된 값을 허용하지 않는 데이터 컬렉션이다. 이러한 특징 때문에 주로 고유한 값의 집합을 관리할 때 사용된다.

## - **요소 추가**

`add()` 메서드를 사용하여 요소를 추가한다.

```javascript
const mySet = new Set();
mySet.add(1);
mySet.add(2);
mySet.add(2); // 중복된 값은 무시됨
```

## - **요소 확인**

`has()` 메서드를 사용하여 요소의 존재 여부를 확인한다.

```javascript
mySet.has(1); // true
mySet.has(3); // false
```

## - **요소 제거**

`delete()` 메서드를 사용하여 요소를 제거한다.

```javascript
mySet.delete(1);
```

## - **반복**

`for...of` 루프를 사용하여 Set의 요소를 반복한다.

```javascript
for (const item of mySet) {
  console.log(item);
}
```

## **Map**

Map은 키-값 쌍을 저장하는 데이터 구조이다. 키는 고유해야 하며, 각 키에 연결된 값을 저장할 수 있다.

## - **요소 추가**

`set()` 메서드를 사용하여 키-값 쌍을 추가한다.

```javascript
const myMap = new Map();
myMap.set("name", "Alice");
myMap.set("age", 30);
```

##- **요소 확인**
`has()` 메서드를 사용하여 특정 키의 존재 여부를 확인하고, `get()` 메서드를 사용하여 값을 가져온다.

```javascript
myMap.has("name"); // true
myMap.get("age"); // 30
```

## - **요소 제거**

`delete()` 메서드를 사용하여 특정 키의 요소를 제거한다.

```javascript
myMap.delete("name");
```

## - **반복**

`for...of` 루프를 사용하여 Map의 키-값 쌍을 반복한다.

```javascript
for (const [key, value] of myMap) {
  console.log(key, value);
}
```

## 정리

Set과 Map은 데이터를 효과적으로 관리할 수 있는 유용한 자료구조로, 중복을 허용하지 않거나 고유한 식별자로 값을 관리해야 할 때 매우 유용한다.
