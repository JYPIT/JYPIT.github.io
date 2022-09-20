---
layout: page
title: "File Upload"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

0. this unordered seed list will be replaced by toc as unordered list 
{:toc}

## 파일 업로드
### Multer
- 파일 업로드에 사용되는 `multipart/form-data`를 처리하기 위한 node.js 미들웨어다.

🔧 `npm install multer`

Form을 Multipart-Form으로 만들어야한다.

`src/views/edit-profile.pug`
```js
block content 
    form(method="POST" enctype="multipart/form-data")
        label(for="avatar") Avatar
        input(type="file" id="avatar" accept="image/*")
        input(name="nickname" placeholder="nickname" type="text" value=loggedInUser.nickname required)
        input(name="email" placeholder="email" type="email" value=loggedInUser.email required)
        input(type="submit" value="수정하기")
```

### Middleware 생성

### 파일 소유자
id video에 저장하여...

#### populate
```js
const postSchema = new mongoose.Schema({
  fileUrl: { type: String, required: true },
  title: { type: String, required: true, minLength: 1, maxLength: 30 },
  content: { type: String, required: true, minLength: 1, maxLength: 500 },
  createdAt: { type: Date, required: true, default: Date.now },
  hashtags: [{ type: String, trim: true }],
  meta: {
    views: { type: Number, default: 0, required: true },
    likes: { type: Number, default: 0, required: true },
  },
  owner: {
    type: mongoose.Schema.Types.ObjectId,
    required: true,
    ref: "User",
  },
});
```

```js
  const { id } = req.params;
  const post = await Post.findById(id);
  const owner = await User.findById(post.owner);
```

```js
if String(post.owner) === String(loggedInUser._id) 
    a(href=`${post.id}/edit`) 게시글 수정 &rarr;
    br
    a(href=`${post.id}/delete`) 게시글 삭제 &rarr;
```

