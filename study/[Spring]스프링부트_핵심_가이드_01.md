---
layout: page
title: "[Spring] Spring & Spring Boot"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
cover: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

## 스프링(Spring)
> Java 기반의 애플리케이션 프레임워크로 **엔터프라이즈급** 애플리케이션을 개발하기 위한 다양한 기능을 제공.<br>
**엔터프라이즈급: 기업 환경을 대상으로 하는 개발**
<hr>

### 스프링의 특징과 구조
#### 제어 역전 | IoC (Inversion Of Control)

> IoC를 적용한 환경에서는 사용할 객체를 직접 생성하지 않고 객체의 생명주기 관리를 **외부**에 위임.<br>IoC를 통해 DI, AOP 등이 가능.<br>
**외부 : 스프링 컨테이너 또는 IoC 컨테이너**<br>
<hr>

#### 의존성 주입 | DI (Dependency Injection)
![image](/assets/study/spring/springBoot/springLogo.png)
> 제어 역전의 방법 중 하나로 외부 컨테이너가 생성한 객체를 주입받아 사용하는 방식.

##### 의존성 주입 받는 방법
- 생성자를 통한 의존성 주입
![image](/assets/study/spring/springBoot/di_constructor.png)
- 필드 객체 선언을 통한 의존성 주입
![image](/assets/study/spring/springBoot/di_field.png)
- setter 메서드를 통한 의존성 주입<br>
![image](/assets/study/spring/springBoot/di_setter.png)
<hr>

#### 관점 지향 프로그래밍 | AOP (Aspect Oriented Programming)
> **관점**을 기준으로 묶어 개발하는 방식.
**관점 : 핵심 기능과 부가 기능으로 나뉜다.

##### AOP 구현하는 방법 세가지
- 컴파일 과정에 삽입하는 방식
- 바이트코드를 메모리에 로드하는 과정에 삽입하는 방식
- 프록시 패턴을 이용한 방식
<hr>

## 스프링 부트(Spring Boot)
![image](/assets/study/spring/springBoot/springBootLogo.png)
> 스프링이 제공하는 다양한 프로젝트 중 하나로 모듈 추가로 인해 설정이 복잡해지는 문제를 해결하기 위해 등장.
<hr>

### 스프링 부트의 특징
#### 의존성 관리
#### 자동 설정 
#### 내장 WAS
#### 모니터링

### 스프링 부트의 동작 방식
> spring-boot-starter-web 모듈을 사용하면 기본적으로 톰캣(Tomcat)을 사용하는 스프링 MVC 구조를 기반으로 동작.
<hr>

## 스프링 부트 웹 애플리케이션 개발에 필요한 지식
### 레이어드 아키텍처
> 애플리케이션의 컴포넌트를 유사 관심사를 기준으로 묶어 수평적으로 구성한 구조.
<hr>

#### 프레젠테이션 계층
- 애플리케이션의 최상단 계층, 클라이언트의 요청을 해석하고 응답.
- UI나 API를 제공.
- 비즈니스 계층으로 요청을 위임하고 받은 결과를 응답.

#### 비즈니스 계층
- 애플리케이션이 제공하는 기능을 정의하고 세부 작업을 수행하는 도메인 객체를 통해 업무를 위임.
- DDD(Domain Driven Design) 기반의 아키텍처에서는 비즈니스 로직에 도메인이 포함되기도 하고, 별도로 도메인 계층을 두기도 함.

#### 데이터 접근 계층
- DB에 접근하는 일련의 작업을 수행.

### 디자인 패턴

#### 생성 패턴

#### 구조 패턴

#### 행위 패턴

<hr>


<hr>
<a href="https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=296591989">스프링 부트 핵심 가이드</a> 책을 기반으로 작성하였습니다.