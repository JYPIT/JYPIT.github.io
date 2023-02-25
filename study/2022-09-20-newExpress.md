---
layout: page
title: "Express"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

# Express

## 동기 비동기 처리
## express.json
body를 확인할 수 있다.

## 외부 Middleware

### Cors
클라이언트와 서버가 동일한 IP를 사용한다면 데이터를 주고 받을 수 있지만 
IP가 다르다면 데이터를 주고 받을 수 없다.

헤더에 `Access-Control-Allow-Origin`를 추가하여 허가할 수 있다.

방법 1. `res.setHeader`를 이용하여 직접 헤더에 추가한다.
방법 2. `cors` 라이브러리 설치하여 사용

### Morgan
클라이언트에서 요청한 정보를 확인할 수 있다.
### Helmet
### cookie-parser
cookie를 확인할 수 있다.
