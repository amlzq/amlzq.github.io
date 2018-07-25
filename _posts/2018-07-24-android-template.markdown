---
layout: post
title:  "Android 项目开发模板"
date:   2018-07-24 00:00
categories: jekyll update
---
* 为了快速开发

### 构建模板android项目仓库
* 必要的类
```
GlobalApplication
Config
```
```
@Override
protected void onDestroy() {
    super.onDestroy();
    handler.removeCallbacksAndMessages(null);
}
```
### AndroidTeamplate
* 开发Android应用样板工程
* 开速快发，快速搭建框架
* jar,so,res较多的第三方类库使用module管理
* core核心包里面放android-support-base代码
* 开发规范
```
* Activity命名规范：XxxActivity
* 布局文件命名规范：将Activity名称的单词顺序颠倒过来并全部转换为小写字母，然后在单词间加下划线：activity_xxx
* 对于xml文件中的尺寸和文字显示采取引用的方式：@dimen/xxx、@string/xxx
* 成员变量名称采用m前缀，是Android编程应遵循的命名规范：private Button mButton
* Android应用属于典型的事件驱动类型。
* 采用匿名内部类实现监听的好处：1，可以在同一处实现监听方法，代码更清晰可读 2，更加符合面向对象的编程思想
* 应用程序设计上：应用展现层与逻辑层尽量分开
```