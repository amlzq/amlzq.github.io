---
layout: post
title:  "对接Google In-App Billing"
date:   2018-05-24 23:49 +0800
categories: jekyll update
---

- 遇到问题首选官方文档和官方客服，血的教训，增加内购代码只要1个小时，发布应用和测试内购需花了10多天。
- 自己解决翻墙问题

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

### Error checking for billing v3 support. (response: 3:Billing Unavailable)
- 问题详情
```
设定应用内结算时出现问题：Error checking for billing v3 support. (response: 3:Billing Unavailable)
```
- 解决方法
```
Google账号地区和内购商品销售地区需要一致
```
- 通过修改Google Pay付款资料来修改账号国家/地区(https://pay.google.com/payments/u/0/home?bcn=98434150854#settings)

- 参考
- [更改您的家庭住址或帐单邮寄地址](https://support.google.com/pay/answer/7644076?visit_id=636378051363455754-1016862153&rd=1#)
- [怎么切换google play 地区?](https://www.zhihu.com/question/21999528)

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
- [个人开发者Google Play上架经验](https://www.jianshu.com/p/0b0664910f41)