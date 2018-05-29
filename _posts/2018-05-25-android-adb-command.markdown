---
layout: post
title:  "Android ADB命令"
date:   2018-05-25 18:00 +0800
categories: jekyll update
---
# 使用adb命令

## 第一步

* 配置环境变量 Android adb/aapt命令
> name
```
ANDROID_HOME
```
> value
``` 
;D:\Android\sdk\platform-tools;D:\Android\sdk\tools;D:\Android\sdk\build-tools\25.0.0
```

## 第二步
* 进入shell命令模式
```
adb shell 
```
* 退出shell命令模式
```
ctrl+c
exit/ctrl+d
```

## 第三步
* 

* 真机运行应用，可以实时查看当前正在运行的Activity
```
logcat | grep ActivityManager
```
* 查看Android 权限
```
adb shell pm list permissions -d -g
```
* 快速打开应用详情页
```
adb shell am start  -a "android.settings.APPLICATION_DETAILS_SETTINGS" -d "package:$1"
```
* 查看最顶层activity名称
```
windows: adb shell dumpsys activity | findstr "mFocusedActivity"
linux: adb shell dumpsys activity | grep "mFocusedActivity"
```
* 查看devices id
```
adb devices
```
* 日志命令
```
adb -s <devices id> shell setprop log.tag.Volley VERBOSE	查看日志
adb shell stop	关闭日志
```
## 查看设备当前的activity
* adb shell dumpsys activity top

## log
* adb shell setprop log.tag.Main V

## 
* adb shell pm clear <package name>
---

# 参考文章
* debug路径: C:/Users/%USERPROFILE%/.android/debug.keystore
* [Authenticating Your Client][Authenticating_Your_Client]

[Authenticating_Your_Client]: https://developers.google.com/android/guides/client-auth?hl=zh-cn