---
layout: post
title: "[자바스크립트] #0. 자바스크립트"
subtitle: "javascript"
categories: study
tags: javascript
---

### JavaScript

-----

- 브라우저 내에서 실행되는 프로그램을 개발할 수 있는 프로그래밍 언어.
  - 모든 브라우저들이 JavaScript를 실행할 수 있는 기능이 있다.
  - JavaScript로 node.js를 개발했는데 이는 브라우저 밖에서도 JavaScript가 실행 될 수 있게 하는 실행환경이다<br> (자바로 따지자면 JVM)
  - node.js가 설치되면 브라우저 환경이 아니더라도 실행할 수 있음

* Java와 문법적 유사성이 많아서 쉽게 배울 수 있다.
* 인터프리터(Interpreter) 프로그래밍 언어다.<br>(컴파일 과정없이 소스가 실행파일로 사용된다.)



####  JavaScript로 할 수 있는일

* HTML 컨텐츠 변경
  * 브라우저를 통해서 **현재 보고 있는 웹 페이지**를 변경할 수 있다.
  * HTML 태그의 속성을 변경할 수 있다.
  * HTML 컨텐츠의 속성을 변경할 수 있다.
    * css 변경가능
  * 사용자 상호작용하는 프로그램을 작성할 수 있다.
    * 이벤트 모델을 활용한다.<br>(사용자가 버튼을 누르거나 값을 입력하면 화면이 동적으로 변하는 프로그램을 만들 수 있다.)
  * 브라우저의 도움 없이 서버와 데이터 통신을 할 수 있다.
    * AJAX기술을 활용하면 가능
    * 화면의 새로고침 없이 서버와 데이터 통신을 할 수 있다.(비동기)<br>(지도, 검색창에 검색할 때 추천검색어 등)



#### JavaScript의 특징

* 스크립트 언어(인터프리터 언어) 다.

* 객체지향 프로그래밍 언어다.

* 동적 데이터타입을 지원한다.

  * 자바스크립트의 변수는 값이 저장될 때, 변수의 타입이 그 값의 타입으로 자동변환된다.

    - 편하지만 에러발견이 쉽지 않다.

    - 이를 보완해서 마이크로소프트는 typescript를 개발함

* 자바스크립트의 함수(메소드)는 1급 시민이다.

  * 함수를 변수에 담거나 매개변수로 전달하거나, 반환값으로 전달할 수 있다.
  * 자바의 1급 시민 : 값(정수, 실수, 문자열, boolean ...), 배열, 객체
  * 자바스크립트의 1급시민 : 값(정수, 실수, 문자열, boolean ...), 배열, 객체, 함수

[^1급시민]: 변수에 저장가능, 반환값으로 사용가능, 함수의 인자로 전달가능

![preferences](https://github.com/supremest35/supremest35.github.io/blob/main/assets/img/function_javascript.png?raw=true)



#### JavaScript 프로그램 작성하기

----

- 스크립트 태그 내에서 작성하기

  ```html
  <script>
  	// 자바스크립트 코드
  </script>
  ```

* 별도의 자바스크립트 파일 사용

  * app.js와 같은 자바스크립트 파일 작성

  * script태그로 웹문서에 포함시킨다.

    ```html
    <script type="text/javascript" src="app.jsp" />
    ```



#### JavaScript의 기본 문법

- 수행문 작성하기

  - 수행문;		// 수행문의 끝은 세미콜론으로 나타낸다.

  - 수행문         // 세미콜론 생략가능

    

- javascript의 리터럴

  - 숫자

    - 123
    - 3.14

  - 문자열

    - "hello world"
    - 'hello world'

  - 배열

    - 자바의 ArrayList와 비슷
      - [1, 2, 3]
      - ['홍길동', '김유신', '강감찬']

  - boolean

    - true
    - false

  - 객체

    - 자바의 Map과 비슷

      - {}

      - {name:"홍길동", age:20, married:true}

        

* javascript의 데이터 타입

  * 자바스크립트 변수의 데이터 타입은 다이나믹하게 변한다.

  * number 타입

    * 기본적으로 java의 double과 비슷
    * 정수, 실수를 담을 수 있다.

  * boolean 타입

    * true, false

  * string 타입

    * ' ' 또는 " "로 표현된 것

  * array 타입

    * [값, 값, 값]

  * object

    * {이름:값, 이름:값}
    * 값은 number, boolean, string, array, object, undefined, null, **함수**가 가능하다.

  * undefined 타입

    * 변수를 선언하고, 값을 할당하지 않으면 그 변수의 값은 undefined이고, 그 변수의 타입도 undefined다.

  * null 값

    * 객체가 할당되지 않았다.

    * null을 값으로 가지는 변수는 "아무것도 가지고 있지 않다"라는 것을 의미한다.

    * null이 저장된 변수의 타입은 object타입이다.

      

* 변수의 선언과 초기화

  * 변수 선언

    ```html
    <script>
        var x;
    	var x, y, z;	// x와 y와 z는 undefined값을 가지고 타입도 undefined다.
    </script>
    ```

  * 변수 초기화

    ```html
    <script>
    	var x;
    	x = 10;
    	var x = 10;
    	var x = 10, y = "홍길동", z = [1, 2, 3];
    </script>
    ```

    