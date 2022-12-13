---
layout: page
title: "React JS 심화"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list
{:toc}

# React 심화

## styled Components

- className이 자동으로 부여된다.
- styled 뒤에는 유효한 html tag만 가능하다.

🔧 `npm install styled-components`

자동 완성 확장 프로그램<br>
[VScode]<br>
`vscode-styled-components` 설치

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

![image description](/assets\study\react_Image\styledComponent.png)

<hr>
- props 사용하기

```js
const Box = styled.div`
  background-color: ${(props) => props.bgColor};
  width: 100px;
  height: 100px;
`;
return (
  <Box bgColor="teal">
    <Text>Hello</Text>
  </Box>
  <Box bgColor="orange" />
);
```
<hr>

### as
- `as`를 사용하여 속성을 바꿔줄 수 있다. 

```js
function App() {
  return (
    <Father>
      <Btn>Click me 1</Btn>
      <Btn as="a" href="http://naver.com">
        Click me 2
      </Btn>
    </Father>
  );
}
```

페이지 소스 결과<br>
![image description](/assets\study\react_Image\styleComponents_as.png)
<hr>

### attrs
- 한번에 속성을 넣어 줄 수 있다.

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

페이지 소스 결과<br>
![image description](/assets\study\react_Image\styleComponents_attrs.png)
<hr>

### animation 
- 설명

```js
import styled, { keyframes } from "styled-components";

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

### Theme
- 모든 색상을 가지고 있는 Object.

#### 라이트모드 & 다크모드
> index.js
```js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import { ThemeProvider } from "styled-components";

const darkTheme = {
  textColor: "whitesmoke",
  backgroundColor: "#111",
};
const lightTheme = {
  textColor: "#111",
  backgroundColor: "whitesmoke",
};

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <React.StrictMode>
    <ThemeProvider theme={darkTheme}>
      <App />
    </ThemeProvider>
  </React.StrictMode>
);
```
> App.js

```js
import styled from "styled-components";

function App() {
  const Wrapper = styled.div`
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    width: 100%;
    background-color: ${(props) => props.theme.backgroundColor};
  `;
  
  const Text = styled.h1`
    color: ${(props) => props.theme.textColor};
  `;

  return (
    <Wrapper>
      <Text>Hello World:)</Text>
    </Wrapper>
  );
}

export default App;
```
