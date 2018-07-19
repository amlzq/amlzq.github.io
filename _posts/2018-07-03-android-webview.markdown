---
layout: post
title:  "Android WebView使用注意事项"
date:   2018-07-03 00:00 +0800
categories: jekyll update
---

### 远程调试 Android 中的 WebView 加载的网页
* Android 4.4 (KitKat) 开始，使用 Chrome 开发者工具可以帮助我们在原生 Android 应用中远程调试 WebView 网页内容。

#### 第一步
```
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```
#### 第二步
```
确保 USB 连接的前提下，打开 PC 中的 Chrome 浏览器，输入网址
chrome://inspect
点击对应网页下方的 inspect 选项便可以进入开发者工具页
```

### [如何在Android应用中查看WebView中的Javascript错误？](https://stackoverflow.com/questions/14859970/how-can-i-see-javascript-errors-in-webview-in-an-android-app)
```
1. Enable JavaScript on your WebView
2. Set a WebChromeClient
3. Override onConsoleMessage
```

### 参考文章
* [Chrome 开发者工具远程调试 Android 中的原生 WebView](http://yifeng.studio/2017/04/29/debug-android-webview-with-chrome-dev-tools/)