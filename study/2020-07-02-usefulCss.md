---
layout: page
title: "자주 쓰는 CSS 명령어"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

# Hello

## flex

<a href="http://flexboxfroggy.com/#ko">Flex를 이용한 게임하기</a>


### justify-content

### align-items
- 컨테이너 안에서 어떻게 모든 요소들이 정렬하는지를 지정
### align-content
- 여러 줄들 사이의 간격을 지정

인자
flex-start: 여러 줄들을 컨테이너의 꼭대기에 정렬
flex-end: 여러 줄들을 컨테이너의 바닥에 정렬
center: 여러 줄들을 세로선 상의 가운데에 정렬
space-between: 여러 줄들 사이에 동일한 간격을 둠
space-around: 여러 줄들 주위에 동일한 간격을 둠
stretch: 여러 줄들을 컨테이너에 맞도록 림

### direction
row
column

### wrap
nowrap: 모든 요소들을 한 줄에 정렬
wrap: 요소들을 여러 줄에 걸쳐 정렬
wrap-reverse: 요소들을 여러 줄에 걸쳐 반대로 정렬


#### flex-flow
flex(direction + wrap)

## position
- 요소를 배치하는 방법

💡
- block : 한 줄을 모두 차지한다.
- inline : 콘텐츠의 크기 만큼 차지한다.


### static
### relative
### absolute
### fixed
### stickey

https://creamilk88.tistory.com/197 참고

출처: "http://flexboxfroggy.com/#ko"