---
layout: post
title:  "对接Google In-App Billing"
date:   2018-05-24 23:49 +0800
categories: jekyll update
---

* 自己解决翻墙问题

## [Google API For Android](https://developers.google.com/android/)

## 对接Google In-app Billing
* [官方文档](https://developer.android.com/google/play/billing/index.html)
* [对接步骤](https://developer.android.com/google/play/billing/billing_integrate.html)

## [实施步骤](https://developer.android.com/google/play/billing/billing_java_kotlin?hl=zh-cn)


* [官方样例](https://github.com/googlesamples/android-play-billing)

* 支付补单方案
> [iOS的In-app Purchase与Android的In-app Billing](https://blog.csdn.net/darklinden/article/details/49506087)
```
先说订单号，和iOS神奇的transaction id与7.0添加的不靠谱的applicationUsername相比，Android有透传订单号这简直是仁慈…在发起支付前就可以对订单号做跟踪，
直到订单结束都可以匹配到唯一支付，除了需要手动发自己服务器汇报参数之外简直毫无破绽。
接着是Restore，Android没有Unconsumable Purchase，相对应的是consume操作，也就是说，只要您没consume，都可以使用Restore从google服务器要上笔已支付的订单信息！
而且透传订单号在手，何愁对不上账?!当初为了处理可重复购买我在前端起sqlite存receipt数据，为了对应帐号和支付订单各种纠结，
前端不但存一堆不可靠数据，因为需要发服务器对苹果服务器验证，服务器一环报错之后也是掉单，客服天天吵吵…
    但是Android，完全可以全靠google服务器Restore确保单笔订单不丢，支付校验完成后再consume可以重复购买，依靠透传订单号确定订单唯一…简直…完美…
```
> [Unity Android 内购 In-App Billing 实现&测试经历](https://www.jianshu.com/p/af15910535cc)

## 测试

### 
* 将apk上次到封闭式渠道
* 创建封闭式渠道
* 添加测试人员
* 将“加入测试的网址”发给测试人员，需要测试人员加入测试计划中。

## 常见问题

### 检查
```
封闭式渠道


```

### 您所要求的項目目前無法購買
* [解决方法](http://www.coderphrase.com/archives/64)
* 没有成功添加测试人员

---

## 参考文章
* [结算时区分测试订单和正式订单-文末尾](http://wiki.midas.qq.com/post/index/2/32/54/0)