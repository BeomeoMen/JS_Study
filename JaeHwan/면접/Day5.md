## 1. Flex와 Grid의 차이점에 대해서 설명해보세요.

Flexbox는 주로 요소를 한 방향(가로 또는 세로)으로 배치하고 정렬할 때 사용되며, 주로 한 차원(1차원) 레이아웃을 다룹니다.
요소 간 간격을 동적으로 조절하거나 가운데 정렬과 같은 레이아웃 요소를 처리할 때 유용합니다.
예를 들어, 웹 페이지에서 메뉴 항목을 가로로 배열하고 가운데 정렬하려면 Flexbox를 사용합니다.
이때 메뉴 항목들은 한 줄로 나란히 표시됩니다.

반면에 Grid는 가로와 세로 방향에서 요소를 격자 모양으로 배치하고 정렬하는 데 사용됩니다.
Grid는 2차원 레이아웃을 다루며, 복잡한 그리드 레이아웃을 생성하거나 요소 간 정렬을 다룰 때 유용합니다.
요소들을 행과 열로 배치하여 복잡한 디자인을 구현할 수 있습니다.
예를 들어, 이미지 갤러리를 디자인할 때 Grid를 활용합니다.
각 이미지가 행과 열에 배치되어 그리드로 표시되며, 요소들 간의 간격과 위치를 더 정밀하게 제어할 수 있습니다.

간단히 말해, Flexbox는 한 방향(가로 또는 세로) 레이아웃에 유용하며, Grid는 두 방향(가로와 세로) 레이아웃을 다루는 데 더 효과적입니다.

### 예상 질문

Flex와 Grid의 공통점은?
Flexbox와 Grid의 공통점은 두 가지입니다. 첫째, 둘 다 웹 페이지나 앱의 레이아웃을 관리하고 정렬하는 데 사용됩니다.
둘 모두 레이아웃을 구성하고 화면 크기에 따라 반응하는 역할을 합니다. 둘째, 둘 다 CSS를 사용하여 디자인 및 레이아웃을 제어합니다.
Flexbox와 Grid 모두 웹 개발자가 레이아웃을 조정하고 스타일을 적용하는 데 도움을 줍니다.

## 2. 비동기 함수에 대해서 설명해 보세요.

비동기 함수란 프로그램에서 작업을 수행할 때, 결과가 나오기까지 기다리지 않고 다른 작업을 수행할 수 있게 하는 함수입니다.
JavaScript에서 비동기 함수는 주로 네트워크 요청, 파일 읽기, 데이터베이스 쿼리와 같이 시간이 걸리는 작업을 다룰 때 사용됩니다.
이렇게 비동기 함수를 사용하면 프로그램이 멈추지 않고 작업을 계속할 수 있으며, 작업이 완료되면 콜백 함수를 호출하여 결과를 처리합니다.

### 예상 질문

JavaScript에서 비동기 함수는 어떻게 사용하나?
콜백함수
콜백 함수(callback function)는 다른 함수의 인자로 전달되어, 특정 동작이나 로직을 나중에 실행하기 위해 사용하는 함수입니다.
이러한 콜백함수는 주로 비동기적인 상황에서 많이 활용되며, 이벤트 핸들링, 타이머 설정, HTTP 요청 등에서 쓰입니다.

콜백 함수는 함수가 일급 객체로 다루어지기 때문에 가능합니다.
일급 객체란 함수를 변수에 할당하거나, 함수의 인자로 전달하거나, 다른 함수의 반환값으로 사용할 수 있다는 의미입니다.
이렇게 함수를 다른 함수의 인자로 전달하고, 해당 함수가 실행될 때 전달된 함수를 호출하는 것을 콜백이라고 합니다.

예를 들어, setTimeout 함수를 사용하여 일정 시간 후에 함수를 실행하고자 할 때, setTimeout 함수의 인자로 실행할 함수를 전달합니다. 이때 전달된 함수가 콜백 함수입니다.

콜백 함수는 비동기 처리에서 많이 사용되며, 이로 인해 코드가 복잡해질 수 있습니다. 따라서 콜백 함수를 남발하지 않고, 가능한 경우 Promise나 async/await 등의 비동기 처리 패턴을 사용하는 것이 좋습니다.

Promise
자바스크립트의 Promise는 비동기 처리를 위한 객체로, 비동기적으로 실행되는 작업의 결과를 대기하고 있을 수 있게 해줍니다.
Promise를 사용하면 비동기 작업을 보다 쉽게 관리할 수 있으며, 비동기적으로 실행되는 코드의 가독성도 높아집니다.

Promise의 3가지 상태는 다음과 같습니다.

1.대기(pending): 비동기 처리가 아직 완료되지 않은 상태입니다.

2.이행(fulfilled): 비동기 처리가 완료되어 결과값을 반환한 상태입니다.

3.거부(rejected): 비동기 처리가 실패하거나 오류가 발생한 상태입니다.

Promise 객체를 생성할 때는 new 키워드를 사용하며 Promise 객체의 생성자 함수는 인자로 executor 함수를 받습니다.
executor 함수는 resolve와 reject 두 개의 콜백 함수를 받습니다.

Promise는 비동기 작업이 맞이할 미래의 완료 또는 실패의 그 결괏값을 나타내는 대리자로, 비동기 연산이 종료된 이후에 결괏값과 실패 사유를 처리하기 위한 처리기를 연결할 수 있습니다.
프로미스를 사용하면 비동기 메서드에서 마치 동기 메서드처럼 값을 반환할 수 있습니다. 다만 최종 결과를 반환하는 것이 아니고 미래의 어떤 시점에 결과를 제공하겠다는 '약속'을 반환합니다.

async/await
async/await은 비동기 프로그래밍을 간편하게 작성할 수 있도록 도와주는 JavaScript의 기능입니다. 이 기능을 사용하면 콜백 함수를 사용하지 않고도 비동기 작업을 간편하게 작성할 수 있습니다.

async 함수는 Promise를 반환하는 함수이며, await은 async 함수 내에서 Promise의 결과를 기다렸다가 반환값을 변수에 할당하는 키워드입니다.
async/await을 사용하면 코드가 더 간결하고 읽기 쉬워지며, 비동기 작업을 처리하는 과정에서 발생할 수 있는 오류를 쉽게 파악할 수 있습니다.

## 3. this에 대해 설명해주세요. (call, apply, bind에 대해 설명해주세요.)

자바스크립트에서 this는 현재 실행 중인 함수의 컨텍스트를 나타내는 특별한 키워드입니다. this의 값은 호출 방식에 따라 동적으로 결정됩니다. 함수는 다양한 방식으로 호출될 수 있으며, 일반적으로 다음과 같은 네 가지 방식으로 호출됩니다.

일반 함수로 호출: 일반 함수로 호출된 경우, this는 전역 객체(window 또는 global)를 참조합니다. 엄격 모드에서는 undefined가 됩니다.
객체의 메서드로 호출: 객체의 메서드로 호출된 경우, this는 메서드를 소유한 객체를 참조합니다.
생성자 함수로 호출: 생성자 함수로 호출된 경우, this는 생성된 객체를 참조합니다.
화살표 함수로 호출: 화살표 함수로 호출된 경우, this는 전역 객체를 참조합니다.
따라서, this는 함수가 어디서 호출되었는지가 아니라 어떤 형태로 호출되었는지에 따라서 결정됩니다. 이를 이해하고 사용하면 자바스크립트에서 객체를 조작하고 메서드를 호출하는 데 유용합니다.

### 예상 질문

call, apply, bind에 대해 설명해주세요

call: 함수를 호출하면서 특정 객체를 함수 내부에서 this로 사용하도록 합니다. 그리고 추가 매개변수를 개별로 전달합니다.

```js
const person = {
  name: "John",
};

function sayHello(age) {
  console.log(`Hello, ${this.name}. I am ${age} years old.`);
}

sayHello.call(person, 25); // 출력: "Hello, John. I am 25 years old."
```

apply: 함수를 호출하면서 call과 마찬가지로 특정 객체를 this로 사용하도록 합니다. 그러나 인수(매개변수)를 배열 형태로 전달합니다.

```js
const person = {
  name: "Alice",
};

function introduceTo(city, country) {
  console.log(`Hi, I'm ${this.name}. I live in ${city}, ${country}.`);
}

introduceTo.apply(person, ["New York", "USA"]); // 출력: "Hi, I'm Alice. I live in New York, USA."
```

bind: 함수를 래핑(감싸는)하고, 새로운 함수를 반환합니다. 반환된 함수는 원본 함수가 실행될 때 항상 특정 객체를 this로 사용하도록 "고정"시킵니다.

```js
const car = {
  brand: "Toyota",
  model: "Camry",
};

function describeCar(year, color) {
  console.log(`This is a ${color} ${year} ${this.brand} ${this.model}.`);
}

const boundFunction = describeCar.bind(car, 2022);
boundFunction("blue"); // 출력: "This is a blue 2022 Toyota Camry."
```

이런 식으로 call, apply, bind를 사용하여 함수 실행 컨텍스트를 설정하고 인수를 제어할 수 있습니다.
