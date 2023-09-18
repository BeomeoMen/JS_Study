# DOM

DOM (Document Object Model)은 JavaScript를 사용하여 웹 페이지의 구조, 콘텐츠 및 스타일에 대한 프로그래밍 방식으로 접근하는 데 사용되는 중요한 개념이다.
이 글에서는 DOM에 대해 상세하게 설명하겠다.

## 1. DOM이란 무엇인가요?

DOM은 HTML 문서나 XML 문서의 구조를 나타내는 표현 방법이다.
즉, 웹 페이지의 모든 요소를 객체로 표현하고, 이러한 객체를 사용하여 웹 페이지의 콘텐츠나 스타일을 동적으로 변경할 수 있다.
HTML 문서는 브라우저에 의해 파싱되고, 파싱된 결과는 트리 구조로 표현된다.
이러한 트리 구조를 DOM 트리라고 부르며, 이를 통해 웹 페이지의 각 요소에 접근하고 조작할 수 있다.

## 2. DOM의 구조

DOM 트리는 다음과 같이 구조화된다.

### Document:

문서 자체를 나타내며, 대개 `<html>` 요소를 포함한다.

### Element

문서의 요소를 나타낸다. HTML 요소는 대개 태그(`<div>`, `<p>`, `<a>` 등)로 표현된다.

### Attribute

요소의 속성을 나타낸다. 예를 들어, `<img src="example.jpg">`에서 `src`는 속성이다.

### Text

요소 내부의 텍스트를 나타낸다. `<p>Hello, World!</p>`에서 "Hello, World!"가 텍스트 노드이다.
이러한 구조를 사용하여 웹 페이지의 모든 요소에 접근하고 조작할 수 있다.

## 3. DOM 조작

JavaScript를 사용하여 DOM을 조작할 수 있으며, 다음과 같은 작업을 수행할 수 있다.

### 3.1 요소 선택

특정 요소를 선택하려면 `document.querySelector()` 또는 `document.getElementById()`와 같은 메서드를 사용한다.

```js
const element = document.querySelector(".my-class"); // 클래스로 요소 선택
const elementById = document.getElementById("my-element"); // ID로 요소 선택
```

### 3.2 요소 속성 변경

선택한 요소의 속성을 변경할 수 있다.

```js
element.setAttribute("src", "new-image.jpg"); // 속성 변경
element.style.backgroundColor = "blue"; // 스타일 변경
element.textContent = "New Text"; // 텍스트 내용 변경
```

### 3.3 요소 추가 및 삭제

새로운 요소를 추가하거나 기존 요소를 삭제할 수 있다.

```js
const newElement = document.createElement("div"); // 새로운 요소 생성
element.appendChild(newElement); // 자식 요소로 추가
element.removeChild(childElement); // 자식 요소 삭제
```

### 3.4 이벤트 처리

DOM 요소에 이벤트 리스너를 추가하여 사용자 상호 작용에 대응할 수 있다.

```js
element.addEventListener("click", () => {
  alert("요소가 클릭되었습니다!");
});
```

## 4. DOM과 웹 애플리케이션

DOM은 웹 애플리케이션 개발에서 중요한 역할을 한다. 웹 페이지의 동적 요소를 관리하고 사용자와 상호 작용하는 데 필수적이다.
JavaScript와 함께 DOM을 사용하면 다음과 같은 작업을 수행할 수 있다.

### 폼 데이터 검증 및 제출

사용자가 입력한 데이터를 검증하고 서버로 전송한다.

### 애니메이션 및 효과

요소의 위치, 크기, 스타일을 변경하여 애니메이션과 효과를 생성한다.

### 동적 콘텐츠 로딩

AJAX를 사용하여 서버에서 데이터를 비동기적으로 로드하고 페이지에 추가한다.

### 이벤트 처리

클릭, 마우스 오버, 키보드 이벤트 등 사용자 상호 작용을 처리한다.
페이지 조작 웹 페이지의 구조를 동적으로 변경한다.

## 5. 요약

DOM은 JavaScript를 사용하여 웹 페이지의 구조와 콘텐츠를 동적으로 조작하기 위한 중요한 도구이다.
DOM을 통해 HTML 문서의 모든 요소에 접근하고 변경할 수 있으며, 이를 통해 웹 애플리케이션의 동작을 제어하고 사용자와 상호 작용할 수 있다.
DOM은 웹 개발에서 핵심 개념 중 하나이며, 웹 페이지의 동적인 특성을 만들어낸다.
