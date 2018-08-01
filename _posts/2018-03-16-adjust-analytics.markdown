---
layout: post
title:  "Adjust数据统计"
date:   2018-03-16 22:03:00 +0800
categories: jekyll update
---
### 在海外市场，你可能会在投放这些广告
```
Facebook Mobile Ads
Google Adwords
Twitter Ads
```
那么就需要第三方监测后台，可选项有[adjust][adjust]，[appsflyer][appsflyer]，[kochava][kochava]。下面是比对这三家的优缺点。
---
#### 介绍[adjust][adjust]
###### 服务功能
* 管理帐户，事件追踪，跟踪链接生成，跟踪第三方商店和预安装推广，使用回调，Facebook移动测量，用adjust跟踪再营销活动，受众分群工具，特殊伙伴，GOOGLE ADWORDS跟踪，TWITTER移动测量指南，同期群分析，KPI服务，深度链接，展示跟踪，防作弊套件，收入验证，SDK签名。

###### 收费标准

###### 权限管理

###### 支持的广告平台
* 覆盖所有主流广告平台

###### 支持的移动应用平台
* AppStore
* Google Play
* Amazon Appstore
* Windows Phone
* Windows Store

```
adb shell am broadcast -a com.android.vending.INSTALL_REFERRER -n com.your.appid/com.adjust.sdk.AdjustReferrerReceiver --es "referrer" "adjust_reftag%3Dabc1234%26tracking_id%3D123456789%26utm_source%3Dnetwork%26utm_medium%3Dbanner%26utm_campaign%3Dcampaign"
```

---
#### 比对[adjust][adjust] 和 [appsflyer][appsflyer]
* 
---
### 参考文章
* [市场常用的3家第三方跟踪渠道大对比](http://www.baijingapp.com/article/2649)
* [adjust/appsflyer这两家移动广告第三方监测工具哪家好用](https://www.zhihu.com/question/31844708)

[adjust]: https://www.adjust.com/
[adjust_android]: https://docs.adjust.com/zh/sdk/android/
[appsflyer]: https://www.appsflyer.com/
[appsflyer_android]: https://support.appsflyer.com/hc/en-us/categories/201114756-SDK-Integrations
[kochava]: https://www.kochava.com/
[kochava_android]: https://support.kochava.com/sdk-integration/sdk-kochavatracker-android