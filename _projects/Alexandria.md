---
layout: project
title: 'Library of Alexandria'
caption: 책의 정보를 얻고 소통할 수 있는 앱.
description: >
  React JS를 이용하여 만든 ...앱.
date: 1 Feb 2023
image: 
  path: /assets/img/project_img/book-in-book.jpg
links:
  - title: Link   
    url: https://qwtel.com/
sitemap: false
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

# Alexandria
## 소개
- TV 프로그램 "신비한 잡학사전"과 한가지 주제를 갖고 다양한 분야의 사람들과 소통하는 공간을 만들고자 앱을 만들었다.
## 기술 스택
### 언어
JS, NodeJS, React, MYSQL
### 프레임워크
### 라이브러리 

## Express

## BOOK API 선정 기준

## 초반 구성
DB 관련<br> 
Firebase
- Real Time DB
- Auth
## 후반 구성
Mysql
- DB 구성

## style
styled-components
좀 더 빠르고 직관적으로 코드를 짜기 위해 사용 하였다.

## 문제와 해결
### Client
#### [User] 새로고침 시 user 정보 공백이 생김
>새로고침 시 `AuthContext`가 리렌더링되면서 user 정보를 다시 가져온다.<br>
이 부분에서 user의 정보가 잠시 사라진다.

- 방법 1. user 상태의 초기값을 {} 빈 객체로 설정하고 user를 일시적으로 true로 반환하게 한 후 받아온다.
- 방법 2. login 시 user를 localStorage에 저장하여 리렌러딩에 상관없이 유지한다 .
#### 페이지 이동 시 Scroll 위치
> 문제: 페이지 이동 시 scroll이 이동 전 위치에 머물러 있다.

- 방법 1. React는 상태를 변경하지 않으면 그 상태를 유지하기 때문에 `ScrollToTop` 함수를 사용하여 다시 페이지를 상단부터 보여줄 수 있게 하였다.

#### [BookGrid] like
> 문제: like가 즉시 반영되지 않는다.
- 방법 1. Item을 다시 가져온다.
- 방법 2. 배열을 따로 저장하여 useMutation으로 캐시를 unvlalidate.<br>

#### [Comment] 댓글
> 문제: `<br />` 태그를 string으로 인식하여 줄바꿈이 정상적으로 동작하지 않는다.<br>
- 방법 1. 문자열을 state에 regex를 사용하여 replace 해준다.<br> 위 방식은 결국 `<br/>`태그를 다시 string으로 인식하기 때문에 정상 동작하지 않는다.<br>

- 방법 2. 문자열을 split하고 map을 이용하여 사이사이에 `<br/>`태그를 심어준다.<br>

- 방법 3. CSS white-space: pre-line 사용하기.<br> white-space: pre-line : 연속 공백 유지. 줄 바꿈은 개행 문자와 `<br>` 요소에서 일어나며, 한 줄이 너무 길어서 넘칠 경우 자동으로 줄을 바꿔준다.<br>

#### textarea Submit
> 문제: 댓글 입력 시 영문은 정상적으로 출력되지만 한글은 마지막 문자가 한번 더 출력된다.
- 방법 1. event.nativeEvent.isComposing === false<br> 한글로 받은 문자열의 마지막 문자가 조합으로 인식되어 나타나기 때문에 위의 코드를 false로 지정하여 출력한다.
#### textarea 자동 높이 조절
> 문제: textarea 높이 조절이 되지 않는다.<br>
- 방법 . useRef를 사용하여 textarea를 참조하고 `textarea.style.height`를 현재`scrollHeight`로 초기화하여 해결 하였다.
#### delete 후 댓글 중복 작성
클래스 내부에서 일처리 후 

### Server
GET에서 BODY를 요청함 
`TypeError: Failed to execute 'fetch' on 'Window': Request with GET/HEAD method cannot have body.` 에러 반환

params에 넣어 해결

#### 배너 이미지 저장 (Multer)
- Error: Multipart: Boundary not found

- MulterError: Unexpected field
multersms input 태그의 name이나 FormData 안의 key값을 통해 파일을 식별한다.

#### blocked by CORS policy
방법 1. JSONP

## 더 나아갈 방향
### 작가와의 소통
### API 더 빠르게 가져오기
### 이용자 차단
### Chat Bot


