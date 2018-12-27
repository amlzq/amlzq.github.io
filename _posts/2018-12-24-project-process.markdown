---
layout: post
title:  "移动端项目开发流程"
date:   2018-12-20 10:00
categories: jekyll update
---

### 模块开发
- 产品规划某一个模块的高保真原型图
- UI
- 客户端人员定义接口
- 客户端人员开发模块


- 
```
项目中经常会有上传文件的需求，特别是上传图片。上传图片通常有两种方式：

bitmap通过Base64转为String，这种方式对于客户端最友好，但是对于服务端要复杂些
multipart/form-data 方式
https://juejin.im/entry/5879aa9cb123db005de3a2fa
```

```
一个android文件的Uri地址一般如下： 
content://media/external/images/media/62026
```