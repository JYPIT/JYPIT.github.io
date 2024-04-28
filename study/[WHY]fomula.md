---
layout: page
title: "알아두자 공식"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

## 등차수열
```yml
Sn = n*(a+1)/2
```
## 에라토스테네스의 체 
> 범위 내에서 소수가 아닌 수를 제거하는 방식,<br>마치 체를 통과시키 듯 소수가 아닌 수를 제외시킨다.

## 경우의 수
### 조합( nCr )

$$
\begin{aligned}
  \phi(x,y) &= \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right) \\[2em]
            &= \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j)            \\[2em]
            &= (x_1, \ldots, x_n)
               \left(\begin{array}{ccc}
                 \phi(e_1, e_1)  & \cdots & \phi(e_1, e_n) \\
                 \vdots          & \ddots & \vdots         \\
                 \phi(e_n, e_1)  & \cdots & \phi(e_n, e_n)
               \end{array}\right)
               \left(\begin{array}{c}
                 y_1    \\
                 \vdots \\
                 y_n
               \end{array}\right)
\end{aligned}
$$
ㄴ
조합 공식
{:.figcaption}

### 순열( nPr )
조합한 것의 순서가 있을 때
$$
\begin{aligned}
  \frac{n!}{(n-r)!}
\end{aligned}
$$]

순열 공식
{:.figcaption}

