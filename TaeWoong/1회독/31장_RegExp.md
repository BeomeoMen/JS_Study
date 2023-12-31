# RegExp

## 정규 표현식이란?

- 일정한 패턴을 가진 문자열의 집합을 표현하기 위해 사용하는 형식 언어
- 문자열을 대상으로 패턴 매칭 기능 제공

## 메서드

> RegExp.prototype.exec

- exec 메서드는 인수로 전달받은 문자열에 대해 정규 표현식의 패턴을 검색하여 매칭 결과를 배열로 반환

> String.prototype.match

- String 표준 빌트인 객체가 제공하는 match메서드는 대상 문자열과 인수로 전달받은 정규 표현식과의 매칭 결과를 배열로 반환

## 플래그

| 플래그 | 의미        | 설명                                                       |
| ------ | ----------- | ---------------------------------------------------------- |
| i      | ignore case | 대소문자를 구별하지 않고 패턴을 검색                       |
| g      | Global      | 대상 문자열 내에서 패턴과 일치하는 모든 문자열을 전역 검색 |
| m      | Multi line  | 문자열의 행이 바뀌더라도 패턴 검색을 계속                  |
