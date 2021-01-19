---
layout: post
title: "[스프링프레임워크] #1. 개발환경"
subtitle: "전자정부표준프레임워크"
categories: study
tags: springframeworkㄵ
---

### 전자정부표준프레임워크

----

이클립스가 설치되어 있더라도 전자정부표준프레임워크에서 개발환경을 다운받아서 하는 것이 편한듯.

[전자정부표준프레임워크 포털]: https://www.egovframe.go.kr/

다운로드 - 표준프레임워크 통합다운로드 -  eGovFrameDev-3.10.0-64bit.exe 다운로드

![egovframe](https://github.com/supremest35/supremest35.github.io/blob/main/assets/img/egovframe.png?raw=true)



압축 풀고 eclipse 폴더 안에 eclipse.exe 파일을 실행하면 spring framework로 개발가능



### 혹시

----

원래 사용하던 이클립스에서 도전하고 싶다면...

이게 맞는지는 모르겠으나 mybatis 연동까지는 성공 했음.

이클립스 실행 - Help - Eclipse Marketplace - popular

- Spring Tools 4 설치
- Spring Tools 3 Add-On for Spring Tools 설치



#### Maven 설치

[^Maven]: 자바용 프로젝트 관리 도구<br> 필요한 라이브러리를 특정문서(pom.xml)에 정의해 놓으면 내가 사용할 라이브러리 뿐만 아니라 해당 라이브러리가 작동하는데에 필요한 다른 라이브러리들까지 관리하여 네트워크를 통해서 자동으로 다운받아줌



[Maven]: http://maven.apache.org/

* Download 탭에서 Binary zip archive 설치

* 압축해제

* 압축해제한 경로(/apache-maven-3.6.3)에 repository 폴더 만들기

* apache-maven-3.6.3\conf에 settion.xml 파일 내용 수정

  * 주석 처리된 <localRepository> 를 빼서 위에서 만든 repository 폴더의 경로 작성

    ![mavenRepository](https://github.com/supremest35/supremest35.github.io/blob/main/assets/img/mavenRepository.png?raw=true)



#### 이클립스 Maven 연동

* 이클립스 실행
* Window - Prefercences - Maven - User Settings
  * Global Settings의 값을 conf 폴더의 settiong.xml 경로로 변경 



#### MyBatis DTD 설정 추가

위에서 다운받은 전자정부표준프레임워크에서는 mybatis xml 템플릿을 쉽게 가져올 수 있었으나 여기서는 찾아볼 수 없다.

따로 DTD를 설정해주면 조금 간단하게 mybatis xml 템플릿을 가져올 수 있다.

* Window - Preferences - XML - XML Catalog - User Specified Enrties - Add
*  config 추가
  * Location : http://mybatis.org/dtd/mybatis-3-config.dtd
  * Key type : Public ID
  * Key : -//mybatis.org//DTD Config 3.0//EN

* mapper
  * Location : http://mybatis.org/dtd/mybatis-3-mapper.dtd
  * Key type : Public ID
  * Key : -//mybatis.org//DTD Mapper 3.0//EN

