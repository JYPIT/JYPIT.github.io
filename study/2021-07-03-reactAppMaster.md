---
layout: page
title: "React App Master"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list
{:toc}

# React 심화

## style
### styled Component

- className이 자동으로 부여된다.
- styled 뒤에는 유효한 html tag만 가능하다.

🔧 `npm install styled-components`

자동 완성 확장 프로그램<br>
[VScode] `vscode-styled-components` 설치

```js
import styled from "styled-components";

const Father = styled.div`
  display: flex;
`;
const BoxOne = styled.div`
  background-color: teal;
  width: 100px;
  height: 100px;
`;
const BoxTwo = styled.div`
  background-color: blue;
  width: 100px;
  height: 100px;
`;
const Text = styled.span`
  color: white;
`;

function App() {
  return (
    <Father>
      <BoxOne>
        <Text>Hello</Text>
      </BoxOne>
      <BoxTwo />
    </Father>
  );
}

export default App;
```

결과

![image description](/assets\study\react\styledComponent.png)

<hr>
- 아래와 같이 응용 가능

```js
const Box = styled.div`
  background-color: ${(props) => props.bgColor};
  width: 100px;
  height: 100px;
`;

...

      <Box bgColor="teal">
        <Text>Hello</Text>
      </Box>
      <Box bgColor="orange" />
```
<hr>

#### attrs
- 

```js
const Input = styled.input.attrs({ required: true, minLength: "3" })`
  background-color: teal;
  color: white;
`;

function App() {
  return (
    <Father>
      <Input />
      <Input />
      <Input />
    </Father>
  );
}
```
#### as
- `as`를 사용하여 속성을 바꿔줄 수 있다. 

```js
function App() {
  return (
    <Father>
      <Btn>Hello</Btn>
      <Btn as="a">Bye</Btn>
    </Father>
  );
}
```
<hr>

### animation 

```js
import styled, { keyframes } from "styled-components";

...

const rotationAnimation = keyframes`
from {
transform:rotate(0deg);
}
to{
transform:rotate(360deg);
border-radius: 50%;
}
`;

const Box = styled.div`
  height: 200px;
  width: 200px;
  background-color: teal;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid black;
  animation: ${rotationAnimation} 1s linear infinite;
  span {
    font-size: 30px;
    &:hover {
      font-size: 70px;
    }
    &:active {
      opacity: 0;
    }
  }
`;
```

💡span을 백틱안에 넣어 styled-components를 적용 받을 수 있다.
💡&는 span을 의미한다.
<hr>

## Dark Mode 만들기

