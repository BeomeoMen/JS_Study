# String

## String 메서드

> String.prototype.indexOf
- indexOf 메서드는 대상 문자열에서 인수로 전달받은 문자열을 검색하여 첫 번째 인덱스를 반환
```javascript
const str = 'Hello World';

str.indexOf('l') // 2

str.indexOf('or') // 7

// 검색 실패 시 -1
str.indexOf('x') // -1
```

> String.proototype.search
- search 메서드는 대상 문자열에서 인수로 전달받은 정규 표현식과 매치하는 문자열을 건색하여 일치하는 문자열의 인데스를 반환.
- 검색에 실패하면 -1 반환

>  String.prototype.includes
- ES6에 도입된 includes 메서든는 대상 문자열엣 인수로 전달받은 문자열이 포함되어 있는지 확인하여 true 또는 false 반환

> String.prototype.startsWith
- ES6에서 도입된 startsWith 메서드는 대상 문자열이 인수로 전달받은 문자열로 시작하는지 확인하여 그 결과를 true 또는 false반환

> String.prototype.endsWith
- ES6에서 도입된 endsWith 메서드는 대상 문자열이 인수로 전달받은 문자열로 끝나는지 확인하여 그 결과를 true 또는 false반환

> String.prototype.charAt
- charAt 메서드는 대상 문자열에서 인수로 전달받은 인덱스에 위치한 문자를 검색하여 반환

```javascript
const str = 'Hello';
for(let i = 0; i < str.length; i++){
    console.log(str.charAt(i)) // H e l l o
}
```

> String.prototype.substring
- substring 메서드는 대상 문자열에서 첫 번째 인수로 전달받은 인덱스에 위치하는 문자부터 두 번째 인수로 전달받은 인덱스에 위치하는 문자의 바로 이전 문자까지 부분 문자열을 반환

```javascript
const str = 'Hello world';

str.substring(1, 4) // ell
```

> String.prototype.slice
- slice 메서드는 substring 메서드와 동일하게 동작
- 단, slice 메서드는 음수인 인수를 전달할 수 있다.
- 음수인 인수를 전달하면 대상 문자열의 가장 뒤에서부터 시작하여 문자열을 잘라내어 반환

> String.prototype.toUpperCase
- toUpperCase 메서드는 대상 문자열을 모두 대문자로 변경한 문자열을 반환

> String.prototype.toLowerCase
- toLowerCase 메서드는 대상 문자열을 모두 소문자로 변경한 문자열을 반환

> String.prototype.trim
- trim 메서드는 대상 문자열 앞뒤에 공배 문자가 있을 경우 이를 제거한 문자열을 반환

> String.prototype.repeat
- ES6에 도입된 repeat 메서드는 대상 문자열을 인수로 전달받은 정수만큼 반복해 연결한 새로운 문자열을 반환
- 음수이면 RnageError

> String.prototype.replace
- replace 메서드는 대상 문자열에서 첫 번째 인수로 전달받은 문자열 또는 정규표현식을 검색하여 두 번째 인수로 전달한 문자열로 치환한 문자열을 반환

> String.prototype.split
- split 메서드는 대상 문자열에서 첫 번째 인수로 전달한 문자열 또는 정규 표현식을 검색하여 문자열을 구분한 후 분리된 각 문자열로 이루어진 배열을 반환
- 인수로 빈 문자열을 전달하면 각 문자를 모두 분리하고, 인수를 생략하면 대상 문자열 전체를 단일 요소로 하는 배열을 반환