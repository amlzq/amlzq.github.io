---
layout: post
title:  "数据库设计-用户表"
date:   2019-05-14 10:00 +0800
categories: jekyll update
---

### 用户表

- table user
```
用户信息表
user id(用户惟一ID，短，查询，自增)
user open id(类似QQ号码一样的用户惟一ID，可公开)
user nickname
user mobile phone
user email
user wechat
user qq
user weibo
user realname
user idcard
user 
```

- 注意
`不需要username，password字段`
`account抽象表示手机号，邮箱`

- 客户端
```
/**
 * 手机号码正则:
 * 由于工信部放号段不定时，所以建议使用泛解析
 */
String REGULAR_PHONENUMBER = "^([1][3,4,5,6,7,8,9])\\d{9}$";
```
