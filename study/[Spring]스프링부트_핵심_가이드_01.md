---
layout: page
title: "[Spring] Spring Boot란"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
cover: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

## 스프링 부트(Spring Boot)
- 스프링이 제공하는 다양한 프로젝트 중 하나로

### 제어 역전 | IoC (Inversion Of Control)

- IoC를 적용한 환경에서는 사용할 객체를 직접 생성하지 않고 객체의 생명주기 관리를 **외부**에 위임.
- IoC를 통해 DI, AOP 등이 가능.

**외부 : 스프링 컨테이너 또는 IoC 컨테이너**<br>

### 의존성 주입 | DI (Dependency Injection)
- 제어 역전의 방법 중 하나로 외부 컨테이너가 생성한 객체를 주입받아 사용하는 방식.

#### 의존성 주입 받는 방법
- 생성자를 통한 의존성 주입
ex)

![image](/assets/study/spring/springBoot/의존성주입_생성자.png)

- 필드 객체 선얼을 통한 의존성 주입
ex)

![image](/assets/study/spring/springBoot/의존성주입_필드객체.png)
- setter 메서드를 통한 의존성 주입

ex)
![image](/assets/study/spring/springBoot/의존성주입_setter.png)
### 관점 지향 프로그래밍 | AOP (Aspect Oriented Programming)
- 관점을 기준으로 묶어 개발하는 방식.

#### AOP 구현하는 방법 세가지
- 컴파일 과정에 삽입하는 방식
- 바이트코드를 메모리에 로드하는 과정에 삽입하는 방식
- 프락시 패턴을 이용한 방식

### 스프링 부트의 동작 방식

### 레이어드 아키텍처
#### 프레젠테이션 계층
#### 비즈니스 계층
#### 데이터 접근 계층
### 디자인 패턴
#### 생성 패턴
#### 구조 패턴
#### 행위 패턴




