---
layout: post
title: "[자바스크립트] #1. 호이스팅(Hoisting)"
subtitle: "변수 호이스팅"
categories: study
tags: javascript hoisting
---

## 변수 호이스팅(Hoisting)

-----

* 함수 내에서 선언되 모든 변수를 함수의 첫번째 수행문 보다 위로 끌어올린다.

* 따라서 모든 변수 선언을 첫번째로 진행하고 코드를 작성하자

  ```html
  <script>
  	function sample1() {
          console.log("a", a);		// a undefined
          console.lig("b", b);		// b undefined
          
          // 변수 a 선언 및 초기화
          var a = 100;
          console.log("a", a);		// a 100
          console.log("b", b);		// b undefined
          
          // 변수 b 선언 및 초기화
          var b = 200;
          console.log("a", a);		// a 100
          console.log("b", b);		// b 200
      }
      
      // 자바스크립트가 실제로 실행하는 코드
      function sample2() {
          var a, b;					// 함수 내에서 선언된 모든 변수를 
          							//함수의 첫번째 수행문 위로 끌어올린다.
          // 변수 a 선언 및 초기화
          var a = 100;
          console.log("a", a);		// a 100
          console.log("b", b);		// b undefined
          
          // 변수 b 선언 및 초기화
          var b = 200;
          console.log("a", a);		// a 100
          console.log("b", b);		// b 200
      }
      
      sample1();
      sample2();
  </script>
  ```

  

#### 자바스크립트의 연산자

* 산술 연산자

  * +, -, *, /, %, ++, --

* 대입 연산자

  * =, +=, -=, *=, /=, %=

* 관계 연산자

* ＞, >=, <=, ==, ===, !=, !==

  * == : 값이 일치하거나, 변환된 값이 일치하면 true

  * **===** : 값이 일치하고 **타입도 일치**하면 true

  * != : 값이 일치하지 않거나, 변환된 값이 일치하지 않으면 true

  * !== : 값이 일치하지 않거나, 타입이 다르면 true

    ```html
    <script>
    	5 == 5		// true
        5 == '5'	// true
        5 === 5		// true
        5 === '5'	// false
        5 != 8		// true
        5 != '8'	// true
        5 !== 5		// false(다른게 하나도 없기 때문)
        5 !== '5'	// ture(타입이 다르기 때문)
    </script>
    ```

* 논리 연산자

  * &&, ∥, !
  * 자바스크립트에서 거짓으로 판단하는 값
    * false, undefined, null, 0, ""
    * 위의 값들이 논리연산자의 값으로 사용되거나 제어문 반복문에서 사용될 때, 거짓으로 판정된다.
    * 논리연산자의 연산결과가 true, false일 수 있지만, true나 false로 판정될 수 있는 1, 100, "vip", null, undefined 등이 될수도 있다.



#### JavaScript 연산자의 특징

* 관계 연산자

  * == : 값만 비교한다. 타입이 다르면 같은 타입으로 변환한 후, 값을 비교한다. 값이 같으면 true
  * != : 값만 비교한다. 타입이 다르면 같은 타입으로 변환한 후, 값을 비교한다. 값이 다르면 true
  * === : 타입과 값이 모두 같으면 true다.
  * !== : 타입이 다르거나 값이 다르면 true다.

* 논리 연산자

* A && B : A와 B 모두 참이면 연산결과도 참이다.

  [^]: A가 거짓이면 B는 체크하지 않는다.

* A ∥ B : A와 B 중 어느 하나가 참이면 연산결과도 참이다.

  [^]: A가 참이면 B는 체크하지 않고 A를 반환한다. A가 거짓이면 B를 반환한다.

* 자바 스크립트에서 거짓이라고 판단하는 값

  * 논리식, if문의 조건식, while문의 조건식, for문의 조건식 ---> 식의 결과가 true 혹은 false를 기대하는 곳

    * 위의 장소에서 아래의 값들은 무조건 거짓으로 판정난다.

      (false, undefined, null, NaN, 0, ' ' ---> 이 값들을 제외하고 모두 참으로 판단)

      ```html
      <script>
      	// name이 비어있으면 false, 그렇지 않으면 true
          if (name) {
              console.log("이름을 확인하였습니다.")
          } else {
              console.log("이름이 비어있습니다.")
          }
      </script>
      ```

      