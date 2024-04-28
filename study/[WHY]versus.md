---
layout: page
title: "[WHY] Versus"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

## toString() vs String.valueOf()
toString()
> null 값이 들어오면 NPE[^1]를 발생시킨다.

[^1]: Null PointerException.

String.valueOf()
> null 값이 들어오면 null 문자열로 반환한다.
