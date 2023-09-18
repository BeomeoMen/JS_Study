# DOM

- DOM은 HTML 문서의 계층적 구조와 정보를 표현하며 이를 제어할 수 있는 API, 즉 프로퍼티와 메서드를 제공하는 트리 자료구조

## 39.1 노드

- 문서노드

  - 최상위에 존재하는 루트 노드(document)
  - window의 document 프로퍼티에 바인딩
  - HTML 문서당 document 객체 유일

- 요소노드

  - HTML 요소를 가리키는 객체
  - 요소 노드는 문서의 구조를 표현

- 어트리뷰트 노드

  - HTML 요소의 어트리뷰트를 가리키는 객체
  - 어트리뷰트 노드에 접근하여 어트리뷰트를 참조하거나 변경하려면 먼저 요소 노드에 접근

- 텍스트 노드

  - HTML 요소의 텍스트를 가르키는 객체
  - 요소노드의 자식 노드

- DOM은 HTML 문서의 계층적 구조와 정보를 표현하는 것은 물론 노드 객체의 종류, 즉 노드 타입에 따라 필요한 기능을 프로퍼티와 메서드의 집합인 DOM API로 제공
- 이 DOM API를 통해 HTML의 구조나 내용 또는 스타일 등을 동적으로 조작 가능

## 39.2 요소 노드 취득

- id를 이용한 요소 노드 취득

  - document.getElementById('id')

- 태그 이름을 이용한 요소 노드 취득

  - document.getElementsByTagName('name')

- class를 이용한 요소 노드 취득

  - document.getElementsByClassName('class')

- CSS 선택자를 이용한 요소 노드 취득
  - CSS 선택자는 스타일을 적용하고자 하는 HTML 요소를 특정할 때 사용하는 문법

## 39.3 노드 탐색

> 자식 노드 탐색

| 프로퍼티                            | 설명                                                                                                                                                                      |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Node.prototype.childNodes           | 자식 노드를 모두 탐색하여 DOM 컬렉션 객체인 NodeList에 담아 반환한다. childNodes 프로퍼티가 반환한 NodeList에는 요소노드뿐만 아니라 텍스트 노드도 포함되어 있을 수 있다.  |
| Element.prototype.children          | 자식 노드 중에서 요소 노드만 모두 탐색하여 DOM 컬렉션 객체인 HTMLCollection에 담아 반환한다. children 프로퍼티가 반환한 HTMLCOllection에는 텍스트 노드가 포함되지 않는다. |
| Node.prototype.firstChild           | 첫 번째 자식 노드를 반환                                                                                                                                                  |
| Ndoe.prottotype.lastChild           | 마지막 자식 노드를 반환                                                                                                                                                   |
| Element.prototype.firstElementChild | 첫 번째 자식 요소 노드를 반환                                                                                                                                             |
| Element.prototype.lastElementChild  | 마지막 자식 요소 노드를 반환                                                                                                                                              |

## 39.6 innerHTML

- 요소 노드의 콘텐츠 영역 내에 포함된 모든 HTML 마크업을 문자열로 반환
- 크로스 사이트 스크립팅 공격에 취약

> 요소 노드 생성

- document.createElement()

> 텍스트 노드 생성

- document.createTextNode()

> 텍스트 노드를 요소 노드의 자식 노드로 추가

- 요소노드.appendChild(텍스트 노드)

> 저장한 위치에 노드 삽입

- Node.insertBefore(newNode, childNode)

> 노드 복사

- Node.cloneNode([deep: true | false])

> 노드 교체

- Node.replaceChild(newChild, oldChild)

> 노드 삭제

- Node.removeChild(child)
