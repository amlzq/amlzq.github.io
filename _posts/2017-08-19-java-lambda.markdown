---
layout: post
title:  "Java Lambda使用简介"
date:   2017-08-19 12:00 +0800
categories: jekyll update
---
### 基本形式
```
Lambda表达式无论怎么变化，都有一个基本的形式：

(参数) -> {表达式}
  其中符号->是不变的，

  参数的变化情况：

无参数
() -> exp
单一参数
param -> exp（自动推导参数类型，可省略()括号）
非单一参数
(param1,param2) -> exp（自动推导参数类型）
(int param1,int param2) -> exp（不能自动推导参数类型）
  表达式的变化情况：

空表达式
param -> {}
单行表达式
param -> exp（可忽略{}括号，返回表达式也可以省略return）
非单行表达式
param -> {exp1;exp2;}(表达式可以是return语句)
  上述的表达方法可能有些抽象，下面我们来举个例子说明下。 就拿前面我们转换出来的Lambda表达式为例：

view -> Log.i("tag","hello lambda")
  这里的view属于参数，Log.i("tag","hello lambda")属于表达式，其中参数属于单一参数，表达式属于单行表达式，所以省略了()和{}这两个括号。
```
---

### 参考文章
* [Android中的Lambda表达式详解](https://maxwell-nc.github.io/android/etrolambda.html#Hello_Lambda%EF%BC%88IDE%E8%87%AA%E5%8A%A8%E8%BD%AC%E6%8D%A2%EF%BC%89)