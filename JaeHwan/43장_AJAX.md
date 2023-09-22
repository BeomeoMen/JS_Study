# AJAX

AJAX는 Asynchronous JavaScript and XML의 약어로, 비동기적으로 서버와 브라우저 간에 데이터를 교환하기 위한 기술이다.
이 기술을 사용하면 페이지 전체를 다시 로드하지 않고도 웹 페이지의 일부분을 업데이트하거나 서버에서 데이터를 가져올 수 있다.

## 1. XMLHttpRequest 객체

AJAX 요청을 만들고 관리하는 주요 객체이다.
이 객체를 사용하여 서버로 데이터를 보낼 수 있고, 서버로부터 데이터를 비동기적으로 받아올 수 있다
다음은 XMLHttpRequest 객체를 생성하는 예제이다.

```javascript
var xhr = new XMLHttpRequest();
```

## 2. 요청 보내기

XMLHttpRequest 객체를 사용하여 서버에 요청을 보낸다.
이때 HTTP 메서드(GET, POST, PUT, DELETE 등)와 요청 URL을 설정하고 필요한 경우 요청 헤더를 추가한다.

```javascript
xhr.open("GET", "https://example.com/api/data", true);
xhr.send();
```

## 3. 비동기 통신

AJAX는 비동기적으로 데이터를 가져오기 때문에 브라우저가 요청을 보낸 후에도 다른 작업을 수행할 수 있다. 이때, 요청이 완료되면 콜백 함수를 호출하여 데이터를 처리한다.

```javascript
xhr.onreadystatechange = function () {
  if (xhr.readyState === 4 && xhr.status === 200) {
    // 요청이 완료되고 응답이 성공적으로 도착한 경우
    var response = xhr.responseText;
    console.log(response);
  }
};
```

## 4. 데이터 형식

AJAX는 주로 XML, JSON, HTML, 텍스트 등 다양한 형식의 데이터를 주고받는다.
응답으로 받은 데이터를 파싱하여 웹 페이지에 적용하거나 화면에 표시할 수 있다.

## 5. CORS (Cross-Origin Resource Sharing)

다른 도메인의 서버로 AJAX 요청을 보낼 때 보안 문제로 인해 브라우저에서 차단될 수 있다.
서버에서 특정 헤더를 설정하여 CORS 문제를 해결할 수 있다.

## 6. 라이브러리 및 프레임워크

AJAX 요청을 보다 쉽게 다루기 위해 jQuery, Axios, Fetch API 등과 같은 라이브러리와 프레임워크를 사용할 수 있다.
이러한 도구들은 더 추상화된 인터페이스와 더 편리한 기능을 제공한다.

```javascript
var xhr = new XMLHttpRequest();
xhr.open("GET", "https://jsonplaceholder.typicode.com/posts/1", true);
xhr.send();

xhr.onreadystatechange = function () {
  if (xhr.readyState === 4 && xhr.status === 200) {
    var response = JSON.parse(xhr.responseText);
    console.log(response.title);
  }
};
```

이 예제에서는 JSONPlaceholder API에서 글 하나를 가져와 제목을 콘솔에 출력하는 간단한 AJAX 요청을 보여준다.

## 정리

AJAX는 비동기적으로 서버와 브라우저 간에 데이터를 주고받는 기술로, 페이지 전체를 새로 고치지 않고 부분적으로 업데이트할 수 있다.
XMLHttpRequest 객체를 사용하여 서버와 통신하며, 비동기 처리와 다양한 데이터 형식을 지원한다. 또한, CORS 문제를 해결하기 위해 서버에서 특정 헤더를 설정할 수 있다.
