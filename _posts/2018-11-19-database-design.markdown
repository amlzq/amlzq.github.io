---
layout: post
title:  "数据库设计"
date:   2018-11-19 10:00
categories: jekyll update
---

### 用户密码设计
* [为什么要在密码里加点“盐”](https://libuchao.com/2013/07/05/password-salt)

- Emoji
```
普通的字符串或者表情都是占位3个字节，所以utf8足够用了，但是移动端的表情符号占位是4个字节，普通的utf8就不够用了，为了应对无线互联网的机遇和挑战、避免 emoji 表情符号带来的问题、涉及无线相关的 MySQL 数据库建议都提前采用utf8mb4字符集，这必须要作为移动互联网行业的一个技术选型的要点。
```
