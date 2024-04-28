---
layout: page
title: "[Java] JSP Tomcat"
author: author1
subtitle: "..."
description: 
category: study
tags: 
    - computer
    - 컴퓨터공학
# hide_description: true
sitemap: true
comments: true
related_posts:
    - study/[컴퓨터공학]02논리게이트.md
cover: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

## JSP란

### TOMCAT

#### Error

##### Cannot resolve method 'print(String)'
문제 해결 Tomcat 폴더에서 아래의 파일들을 직접 추가하여 해결

###### 1. servlet-api.jar 파일 추가
tomcat에서 servlet 컴파일하는 역할을 하는 모듈

###### 2. jsp-api.jar 파일 추가
