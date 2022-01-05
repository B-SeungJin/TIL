# TIL
Today I Leran
12.20 ~ 자바스크립트 공부 시작

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
