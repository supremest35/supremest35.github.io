---
layout: post
title: "[클론코딩] #0. 싸이월드 클론코딩"
subtitle: "초기설정"
categories: project
tags: 개인프로젝트
---

## 초기 설정

### 사용 프로그램

--------------

1. STS
2. Maven
3. Apache Tomcat
4. Oracle
5. SQL Developer
6. Visual Studio Code
7. 네이버 클라우드 플랫폼(서버)



### Spring boot 프로젝트 생성

---

1. Type : Maven

2. Packaging : War

3. Java Version : 11

4. 의존성 추가 : 

    ![preferences](https://github.com/supremest35/supremest35.github.io/blob/main/assets/img/dependency.png?raw=true)



### Vue.js 프로젝트 생성

----

1. 위에서 만든 스프링 부트 프로젝트의 root폴더에서 frontend 폴더 만듦

2. cmd 창에서 frontend폴더로 이동

3. vue init webpack (프로젝트 이름) 으로 설치

   + 여러가지 옵션을 선택하라는게 나오는데 그냥 Enter만 눌러서 진행함

4. 설치 완료되면 완료된 프로젝트 안으로 이동(cd 폴더명)

5. bootstrap-vue 패키지 설치

   + npm install bootstrap-vue bootstrap --save

6. bootstrap-vue Vue.js 프로젝트에 추가

   + main.js

     ```js
     import BootstrapVue from 'bootstrap-vue'
     import 'bootstrap/dist/css/bootstrap.min.css'
     import 'bootstrap-vue/dist/bootstrap-vue.css'
     
     Vue.use(BootstrapVue)
     ```



### bootstrap-vue 사용법

----

[bootstrap-vue]: https://bootstrap-vue.org/docs/components

위의 링크 참고



### 실행

---

- frontend

  ++ cmd창에서 vue.js 프로젝트로 이동

  ++ npm run serve 실행

  ++ 크롬에서 localhost:8081(8080은 이미 사용중)으로 이동하면 화면 출력



* backend

  ++ STS에서 서버 켜고 실행하면됨.



(서버 하나만 켜서 실행하는 방법이 있는지는 모르겠음)