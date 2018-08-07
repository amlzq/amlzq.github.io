---
layout: post
title:  "对接Google OAuth"
date:   2018-05-23 19:49 +0800
categories: jekyll update
---
* 自己解决翻墙问题
* [Google客服帮助](https://support.google.com/googleplay/android-developer#topic=3450769)

## [Google API For Android](https://developers.google.com/android/)

## Google账号登录
* [官方文档](https://developers.google.com/identity/sign-in/android/)

---
* FQA
```
You have wrong OAuth2 related configurations, please check. Detailed error: INVALID_AUDIENCE
```
* 核对requestIdToken的参数，请使用web app client id,not android client id
```
You have wrong OAuth2 related configurations, please check. Detailed error: UNREGISTERED_ON_API_CONSOLE
signInResult:failed code=10
```
---
# 参考文章
* [对接步骤](https://developers.google.com/identity/sign-in/android/sign-in?hl=zh-cn)
* 

[google_play_console]: https://play.google.com/apps/publish/?hl=zh-cn
[try_signin_for_android]: https://developers.google.com/identity/sign-in/android/start?hl=zh-cn
[start_integrating]: https://developers.google.com/identity/sign-in/android/start-integrating?hl=zh-cn#get_your_backend_servers_oauth_20_client_id
[firebase_oauth]: https://firebase.google.com/docs/auth/android/google-signin?hl=zh-cn