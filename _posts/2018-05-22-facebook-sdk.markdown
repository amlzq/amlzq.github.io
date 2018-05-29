---
layout: post
title:  "对接Facebook SDK"
date:   2018-05-22 19:49 +0800
categories: jekyll update
---
### 第一步添加新应用
* 首先登入[Facebook for Developers后台][facebook_developers]
* 在[Facebook for Developers后台][facebook_developers]添加新应用
![]({{ site.baseurl }}/assets/facebook_sdk/add_app.png)

### 第二步设置新应用
![]({{ site.baseurl }}/assets/facebook_sdk/set_app.png)

### 第二步添加产品

#### 这里我们添加`Facebook 登录`和`Facebook Analytics `
![]({{ site.baseurl }}/assets/facebook_sdk/add_product.png)

#### 设置`Facebook 登录`产品，圈中为必填项
![]({{ site.baseurl }}/assets/facebook_sdk/set_login_params.png)

#### 快速启动`Facebook 登录 Android`产品，圈中为必填项
![]({{ site.baseurl }}/assets/facebook_sdk/set_login_params2.png)

* 添加开发密钥散列
```
keytool -exportcert -alias androiddebugkey -keystore "C:\Users\USERNAME\.android\debug.keystore" | "PATH_TO_OPENSSL_LIBRARY\bin\openssl" sha1 -binary | "PATH_TO_OPENSSL_LIBRARY\bin\openssl" base64
样例:
keytool -exportcert -alias androiddebugkey -keystore "C:\Users\asus\.android\debug.keystore" | C:\Users\asus\openssl-0.9.8k_X64\bin\openssl sha1 -binary | C:\Users\asus\openssl-0.9.8k_X64\bin\openssl base64
输入密钥库口令:  android
zLlKaTuvmZF8adWATAUGOZJDYIs=
```

* 添加发布密钥散列
```
keytool -exportcert -alias YOUR_RELEASE_KEY_ALIAS -keystore YOUR_RELEASE_KEY_PATH | openssl sha1 -binary | openssl base64
替换您的发布密钥别名和 keystore 路径
```

### 第三步开启应用状态
> ![]({{ site.baseurl }}/assets/facebook_sdk/start_status.png)
---

# 参考文章
* [官方文档][facebook_developers_docs]

[facebook_developers]: https://developers.facebook.com/
[facebook_developers_docs]: https://developers.facebook.com/docs/apps