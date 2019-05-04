---
layout: post
title:  "Android开发指南"
date:   2017-08-03 00:00 +0800
categories: jekyll update
---

- [Android编码命名规范](http://blog.coderclock.com/2015/12/27/android/Android%E7%BC%96%E7%A0%81%E5%91%BD%E5%90%8D%E8%A7%84%E8%8C%83/)

- [Android Plugin DSL Reference](https://google.github.io/android-gradle-dsl/current/index.html)
```
Gralde命令注解
```

- [安卓开发常用工具和第三方库汇总](https://academy.realm.io/cn/posts/tools-and-libraries-for-common-android-problems/)

- 文件命名参考

- My系列，每个项目必须且唯一的类
- MyApplication extends Application
- MyConfig extends ApplicationConfig
- MyConstant extends ApplicationConstant

- 网络库系列

- SQLite-Room
- MyDatabase extends RoomDatabase
- 


## 基础阶段
- 基础
- 四大组件+SQLite+SP+File+

## 当前阶段
- java+third party components
- android support
- android arch
- MVP
- RxJava+OkHttp+

## 新阶段
拥抱jetpack
- kotlin+jetpack
- androidx
- MVVM
- livedata+room+dagger2+viewmodel

## 新阶段
熟悉iOS，熟悉跨平台
- flluter
- reactnative

## 项目经验
- 游戏盒子APP
- 阅读APP
- 网店APP
- 应用商店APP
- 钱包APP
- 高仿网易云
- 高仿知乎
- 高仿微信

## 目前的帐号体系
- table user
```
用户信息表
user id(类似QQ号码一样的用户惟一ID，可公开)
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
`不需要username，password字段`

- table moment
```
用户动态表

```

- 业务表
```

```
