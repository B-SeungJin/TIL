# TIL
Today I Learn
* 12.20 ~ 01.11 자바스크립트
* 01.17 ~ 01.21 html, css
* 02.03 ~ c언어

## 12.20
* 첫 velog글을 올렸다. 
* 변수 선언시 var키워드를 사용하지 않는 이유, 변수 명명 규칙을 익혔다.
  - var는 전역변수로서 메모리 낭비, 변수 호이스팅으로 인해 흐름이 꼬임. 기호는 $와 _만 가능함.
* 생성자 함수의 내부 동작 프로세스, 내부 메소드, new.target-스코프 세이프 생성자 패턴을 배웠다.
  - return 키워드 쓰지말자. 화살표 함수, 메서드 축약형은 [[Construct]]없어서 생성자 함수X, IE에서는 스코프 세이프 생성자 패턴 사용
## 12.21
* 일급 객체, 프로퍼티 어트리뷰트에 대하여 알아보았다.
  - 자바스크립트의 함수 = 일급 객체 = 일급 함수(값으로 이용 가능), Object.defineProperty() 메서드를 통해 프로퍼티를 정의 가능.
* 다음에 알아 볼 것: symbol.iterator, Es5 와 Es6의 차이 - 함수 선언문은 함수의 이름을 생략할 수 없기 때문에 차이가 없지만, 함수 표현식은 함수의 이름을 생략할 수 있기에 발생하는 차이점 확인, 프로토타입
## 12.22
* 프로토타입 상속, 프로토타입 체인에 대하여 배웠다.
  - 프로토타입은 읽기 전용이라 객체에 직접 프로퍼티를 할당하고, 추가됌. this는 프로토타입에 영향을 받지 않음. for..in은 상속 프로퍼티도 순회대상에 포함. obj.hasOwnProperty(key)는 상속 프로퍼티가 순회대상에서 제외.
* 내장 객체의 프로토타입, 프로토타입에 직접 접근할 수 있는 메서드에 대해 배웠다.
  - 메서드는 프로토타입에 저장, 객체 자체엔 데이터만 저장.
* this binding 종류에 대해 알아보았다. 화살표 함수의 this는 언제나 상위 스코프의 객체(렉시컬 this)를 가리킨다.
## 12.24
* 렉시컬 환경 객체(환경 레코드-변수 저장, 외부 렉시컬 환경에 대한 참조)를 품고 있는 실행 컨텍스트에 관해 배웠다.
  - 객체 환경 레코드가 전역객체를 가르키기에 변수 호이스팅이 일어나고, 렉시컬 환경 객체(외부 렉시컬 환경에 대한 참조)에 의해 스코프 체인이 형성.
* 클로저와 클로저의 올바른 사용방법을 익혔다.
  - 호출이 끝난 후에도 여전히 도달 가능한 중첩 함수는 [[Environment]] 프로퍼티에 외부 함수 렉시컬 환경에 대한 정보가 저장되기 때문임. 내부함수를 즉시 실행함수의 return값으로 설정하고 변수에 할당해 클로저를 올바르게 사용함.
* 다음에 알아볼 것: 클로저 사용방법(더 자세히)
## 12.27
* 벽돌깨기 게임 구현을 하며 이벤트 핸들러 함수를 배웠다.
  - addEventListener 메서드를 통해 여러개의 이벤트 핸들러 등록 가능. 이벤트 위임 과정(캡처, 버블)을 배움.
* HTML5 <canvas>를 구현해보았다.
  - 조금 더 자세히 공부해봐야함.
## 12.28
* 벽돌깨기 게임을 완성하였다.
  - css를 통해 예쁘게 꾸며보고 싶음.
## 12.31
* 클래스(확장 문법, 메서드/생성자 오버라이딩, protected 프로퍼티 등등)에 대하여 공부하였다.
  - 메서드 오버라이딩에서 super()는 화살표함수를 지원X, 자체 정의한 메서드는 상속 시 자체 메서드가 사용. '믹스인'을 통해 다중상속을 지원하지 않는 자바스크립트에, 다수의 메서드를 복사해 프로토타입에 구현 가능.
* 다음에 알아볼 것: 클래스 필드 오버라이딩, 믹스인 적용하기
* 객체의 특징인 가진 자바스크립트 배열, 배열 메서드, 정규 표현식을 알아보았다.
  - 배열 메서드(push, splice, concat등), 플래그(i, g)와 패턴(/.../)이 있음.
* String 객체의 프로퍼티와 메서드, Symbol에 대해 익혔다.
  - 심볼로 정의된 프로퍼티는 열거 불가능.
## 01.03
* 이터레이터에 관해 공부하였다
  - [Symbol.iterator]는 순회할 때마다 호출되는 메서드이며, 이터러블은 [Symbol.iterator] 메서드를 포함한 원본 객체 자체, 이터레이터는 순회할 때마다 새로 반환되는 값(value와 done을 담은 객체)을 의미함.
* 스프레드 문법(concat, splice, slice 대체), rest parameter에 대해 공부하였다.
  - 무언가를 배열로 바꿀 때는 스프레드 문법보다 Array.from이 보편적으로 사용, 배열이나 객체를 복사 시 스프레드 문법 사용.
* 다음에 알아 볼 것: async 이터레이터에 대해 이해하기
## 01.05
* 구조 분해할당을 공부하였다.
  - 데이터 담긴 순서대로 추출(좌변-[], 우변-이터러블), 원하는 값을 추출(좌변-{}, 우변-객체)함. 배열 구조분해할당은 순서가 중요할 때, 객체 구조분해할당은 필요한 데이터가 따로 있을시 사용.
* Set(중복 여부 확인-배열), Map(프로퍼티 key의 타입제한X-객체)에 대해 익혔다.
  - 객체는 [Symbol.iterator] 메서드를 가져야 이터러블이 될 수 있지만, 모든 Map은 이미 이터러블이다.
## 01.06
* 이벤트(버블링, 캡처링)와 이벤트 위임, 타이머 함수에 관하여 익혔다.
  - 이미 존재하는 함수를 직접 핸들러에 할당할때 ()를 붙이지 않음. 핸들러 삭제 시 사용한 함수를 그대로 전달해야 함.
* 다음에 알아 볼 것: 다양한 이벤트 위임 알고 적용하기, debounce, throttle에 대해 자세히 공부하기
## 01.09
* 프로미스(.then/.catch/.finally 메서드), 프로미스 체이닝, async/await에 대해 공부하였다.
  - 결과가 어떻든 마무리가 필요하면 finally가 유용함. async/await를 사용하면 promise.then/catch가 거의 필요 없음.
* 다음에 알아 볼 것: thenable객체에 대해 더 알아보기. fetch의 선택 매개변수 공부하기.
* 제너레이터에 관해 공부하였다
* 에러(catch, throw)를 공부하며 타입스크립트의 중요성에 대하여 알게 되었다.
## 01.11
* 모듈에 관해서 알아보았다.
* 원시타입과 객체타입에 대해 알아보았다.
  - 원시타입은 복사 시 새로운 주소로 바뀌지만, 객체 타입은 복사 시 주소를 유지하는데 Object.freeze()를 통해 이를 방지 가능.
## 01.15
* 순수 자바스크립트를 이용한 간단한 쇼핑몰을 구현하였다.
  - fetch()를 통해 데이터를 동적으로 추가함. map()을 통해 배열을 받아와 다른 형태의 배열로 맵핑함. 템플릿 문자열을 사용함.
* 내가 지금까지 공부한 자바스크립트와는 다루는 방법이 많이 달랐다.
  - 자바스크립트의 웹브라우저에 대해 공부해야함. 더불어 html, css 익숙해지기.
## 01.17
* HTML5 문법에 대해 알아보고 노트에 정리하였다.
  - 시멘틱 태그를 통한 시멘틱 웹 구축하기.
## 01.18
* CSS3 문법인 가상 클래스 셀렉터, display프로퍼티, position프로퍼티 등(1~8편)에 대하여 정리하였다.
## 01.20
* CSS3문법인 캐스캐이딩, 트랜지션, 애니메이션, 트랜스폼 등 (9~16편)에 대하여 정리하였다.
## 01.21
* CSS3문법인 레이아웃(float), 반응형 웹디자인(Media Query), Flexbox, 수평/수직 정렬, Grid System에 대하여 정리하였다.
* Sass에 대해서는 CSS3를 더 능숙하게 다룬 뒤 공부해야겠다.
## 01.26
* 미디어커리를 이용해 반응형 헤더를 만들었다.
  - 자바스크립트를 통해 이벤트 처리를 함.
* 상품 분류에 있어 오류를 수정하였다.
## 02.03
* 복학을 위해 c언어 복습, 예습(포인터부터)을 시작한다.
* 포인터 이전까지의 내용(변수, 자료형 등)을 책을 통해 복습하였다.
  - 2진수, 비트연산자 등을 기억하자.
## 02.04
* 포인터 이전까지의 내용(반복문, 조건문, 함수 등)을 책을 통해 복습하였다.
## 02.06
* 포인터 부분부터는 예습이기에 '윤성우의 열혈 프로그래밍' 강좌를 통해 공부한다.
* 1차원 배열, 포인터의 개념에 대하여 공부하였다.
  - 모든 문자열의 끝에는 널문자 자동 삽입, 없을 시 문자 배열.
  - 포인터 크기 변수는 항상 동일. int *ptr = NULL; 로 초기화 권장. arr[i] == *(arr+i)
