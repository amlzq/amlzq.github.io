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
- table moment
```
用户动态表

```

- 业务表
```

```

### 自定义注解

@ReleaseCheck // 方法/类/字段的发布打包时候检查
@permission // 方法的注解，需要的权限
@author // 方法的注解，作者是否原创，来源是连接
@contribution // 借鉴，参考

### 规范
- 代码中消灭非英文
- 混淆，加固，瘦身
- 渠道包

- ids
```
tv_
iv_
```

- 单词简写
```
description desc

```

`不要随意改类的命名`
