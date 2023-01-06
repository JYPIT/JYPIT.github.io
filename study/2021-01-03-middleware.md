---
layout: page
title: "Middleware 구성하기"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

## Middleware
- 브라우저가 request 한 다음 그리고 서버가 response 하기 전에 그 사이에서 역할을 함

### Middleware 예시 및 과정
예시)
```js
const newMiddleware = (req, res, next) => {
  console.log("I'm Middleware!!");
  next();
};

const handleHome = (req, res) => {
  return res.send("Hello");
};

app.get("/", newMiddleware, handleHome);
```
과정 => 브라우저는 "/(Home)"을 get -> express가 newMiddleware 호출<br>
    -> newMiddleware는 `console.log` 실행 -> next 함수 호출<br>
    -> expresss는 next 함수를 보고 handleHome 호출

∴ 모든 Controller(handler)는 Middleware 혹은 Finalware가 될 수 있다.

#### Global Middleware

`express.use()` 

예시)
```js
const newMiddleware = (req, res, next) => {
  console.log(`"I'm Middleware!!"`);
  next();
};

const handleHome = (req, res) => {
  return res.send("Hello");
};

app.use(newMiddleware);
app.get("/", handleHome);
```
=> 모든 route에서 newMiddleware는 작동한다.

⚠️ use를 사용할 때 순서가 중요하다.

#### Protection Middleware

```js
const logger = (req, res, next) => {
  console.log(`${req.method} ${req.url}`);
  next();
};

const privateMiddleware = (req, res, next) => {
  const url = req.url;
  if (url === "/protected") {
    return res.send("<h1>Not Allowed</h1>");
  }
  console.log("Allowed, you may Continue");
  next();
};

const handleHome = (req, res) => {
  return res.send("Hello");
};

const handleProtected = (req, res) => {
  return res.send("Welcome to the private lounge");
};

app.use(logger);
app.use(privateMiddleware);
app.get("/", handleHome);
app.get("/protected", handleProtected);
```
=> url이 /protected면 접근을 막아준다.

#### Morgan
- Morgan 함수를 호출하면 설정한대로 middleware를 return 해준다.

🛠️ `npm install morgan`

사용 `import morgan from "morgan";`

##### Morgan 옵션 dev
```js
const logger = morgan("dev");
app.use(logger);
```

결과: GET / 304 3.254 ms - -

=> logger보다 더 정교하게 나온다.

##### Morgan 옵션 combined
```js
const logger = morgan("combined");
app.use(logger);
```
- 시간 method, http 버전, 사용중인 브라우저, OS 등 많은 것을 보여준다.

##### Morgan 옵션 그 외

- tiny
- short
- common

<hr>

Continue with [Router](2021-01-03-router.md){:.heading.flip-title}
{:.read-more}

**참고**
<li><a target="_blank" href="https://nomadcoders.co/?gclid=CjwKCAjw2f-VBhAsEiwAO4lNeGxUb10hQEsnXWufl6NE_TMbZVomtR59HvzfaaYKAIONyRIsWAW8QxoCRK0QAvD_BwE">Nomad Coders</a></li>