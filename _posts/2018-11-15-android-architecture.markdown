---
layout: post
title:  "Android架构分析"
date:   2018-11-15 10:00
categories: jekyll update
---

### MVC
- [Model–view–controller](https://zh.wikipedia.org/wiki/MVC)

```
控制器（Controller）- 负责转发请求，对请求进行处理。
视图（View） - 界面设计人员进行图形界面设计。
模型（Model） - 程序员编写程序应有的功能（实现算法等等）、数据库专家进行数据管理和数据库设计(可以实现具体的功能)。
```

- 在Android上实现MVC
- 在使用fragment的情况下
```
activity为controller
fragment为view
所以一个模块一般包含activity/fragment
```

- 项目
- [AndroidMvc](https://github.com/kejunxia/AndroidMvc)

### MVP
- [Model–view–presenter](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93presenter)

- 项目
- [android-architecture](https://github.com/googlesamples/android-architecture)

### MVVM
- [Model–view–viewmodel](https://zh.wikipedia.org/wiki/MVVM)

- 项目
- [android-architecture](https://github.com/googlesamples/android-architecture)

- 实践
- []()

### AAC
- [Android Architecture Components](https://developer.android.com/topic/libraries/architecture/)

- [基于Android Architecture Components的应用架构指南](https://cdc.tencent.com/2017/06/29/%E5%9F%BA%E4%BA%8Eandroid-architecture-components%E7%9A%84%E5%BA%94%E7%94%A8%E6%9E%B6%E6%9E%84%E6%8C%87%E5%8D%97/)

### 其他分析
- [MVC，MVP 和 MVVM 的图示-阮一峰](http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html)
- [MVC、MVP、MVVM架构分析与比较](https://www.jianshu.com/p/8e3d4ab80714)

### 实践MVP + RxJava2 + Retrofit2 + Dagger2+Arouter
* di(Dependency Injection)