# 15장 let, const와 블록 레벨 스코프
### 15.1 var 키워드로 선언한 변수의 문제점

#### 15.1.1변수의 중복 선언 허용 
        
 
- 함수 레벨 스코프<br>
var 변수의 지역 스코프는 오로지 함수의 코드블록만 허용 O  /  if , for 같은 블록은 허용 X
  

    var x = 1
    
    if (true) {
      // x는 전역 변수. 위에 전역 변수가 있어서, 여기의 x는 중복 선언된다.
      // var 키워드는 없는 것 처럼 인식되고, 재할당만 이뤄진다.
      // 의도치 않게 변수값이 변경되는 부작용이 있다.
      var x = 10
    }
    
    console.log(x) // 10
    
    var i = 10
    
    for (var i = 0; i < 5; i++) {
      console.log(i) // 0, 1, 2, 3, 4
    }
    // for 문은 지역 스코프가 아닌 전역 스코프라서 i는 5로 잡힌다.
    console.log(i) // 5
  
- 변수 호이스팅
  
  - var 변수는 호이스팅에 의해 변수 선언 전에도 읽을 수 있으나, 값의 할당 전에 참조하면 언제나 undefined를 반환한다.
  - var 변수는 런타임 이전에 선언 단계와 초기화 단계가 한번에 진행되며, 이때 undefined로 초기화한다.


  
    // 런타임 이전에 선언과 초기화가 실행된다. foo ==== undefined
    // 따라서 변수 선언문 이전에 변수를 참조할 수 있다.
    console.log(foo) // undefined
    
    var foo
    console.log(foo) // undifined
    
    foo = 1 // 할당문에서 할당 단계가 실행된다.
    
    console.log(foo) // 1

## 15.2 let 키워드

var의 문제점을 보완 하기 위해 , ES6 부터 let, const가 등장함.
- 변수 중복 선언 금지, 재할당 불가능

  let은 var처럼 중복 선언을 허용하지 않는다. 하지만 재할당은 가능하다.


- 블록 레벨 스코프
  let은 모든 코드 블록을 지역스코프로 인정하는 블록 레벨 스코프를 따른다.


- 변수 호이스팅
  - var와는 다르게 let은 선언 단계와 초기화 단계가 분리되어 진행된다. 
  - 초기화 전에 호출을 하면 참조 에러가 발생한다. 
  - 일시적 사각지대(TDZ) : 스코프 시작부터 초기화 시점까지 변수를 참조할 수 없는 구간

 
## 15.3 const 키워드
const는 주로 상수를 사용하기 위해 사용된다. let과 대부분은 동일하나 차이점은 다음과 같다
- 선언과 초기화 <br>
  반드시 선언과 동시에 초기화해야한다.

- 재할당 금지 <br>
  let 과는 다르게 재할당은 불가능하다
