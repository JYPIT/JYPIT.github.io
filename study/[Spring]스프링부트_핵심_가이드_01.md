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
> Java 기반의 애플리케이션 프레임워크로 **엔터프라이즈급** 애플리케이션을 개발하기 위한 다양한 기능을 제공.
**엔터프라이즈급: 기업 환경을 대상으로 하는 개발**
<hr>

### 스프링의 특징과 구조
#### 제어 역전 | IoC (Inversion Of Control)

> IoC를 적용한 환경에서는 사용할 객체를 직접 생성하지 않고 객체의 생명주기 관리를 **외부^[1]**에 위임.
> IoC를 통해 DI, AOP 등이 가능.

**[1]외부 : 스프링 컨테이너 또는 IoC 컨테이너**<br>

#### 의존성 주입 | DI (Dependency Injection)
> 제어 역전의 방법 중 하나로 외부 컨테이너가 생성한 객체를 주입받아 사용하는 방식.

##### 의존성 주입 받는 방법
> 생성자를 통한 의존성 주입
![image](/assets/study/spring/springBoot/di_constructor.png)

> 필드 객체 선얼을 통한 의존성 주입
![image](/assets/study/spring/springBoot/di_field.png)

> setter 메서드를 통한 의존성 주입
![image](/assets/study/spring/springBoot/di_setter.png)

<hr>

#### 관점 지향 프로그래밍 | AOP (Aspect Oriented Programming)
> **관점**을 기준으로 묶어 개발하는 방식.
**관점 : 핵심 기능과 부가 기능으로 나뉜다.

##### AOP 구현하는 방법 세가지
- 컴파일 과정에 삽입하는 방식
- 바이트코드를 메모리에 로드하는 과정에 삽입하는 방식
- 프락시 패턴을 이용한 방식

<hr>

## 스프링 부트(Spring Boot)
- 스프링이 제공하는 다양한 프로젝트 중 하나로 모듈 추가로 인해 설정이 복잡해지는 문제를 해결하기 위해 등장.

### 스프링 부트의 특징
#### 의존성 관리
#### 자동 설정 
#### 내장 WAS
#### 모니터링

### 스프링 부트의 동작 방식

### 레이어드 아키텍처
#### 프레젠테이션 계층
#### 비즈니스 계층
#### 데이터 접근 계층
### 디자인 패턴
#### 생성 패턴
#### 구조 패턴
#### 행위 패턴

<hr>


<hr>
<a href="https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=296591989">스프링 부트 핵심 가이드</a> 책을 기반으로 작성하였습니다.