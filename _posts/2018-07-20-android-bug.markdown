---
layout: post
title:  "Android BUG列表"
date:   2018-07-20 00:00
categories: jekyll update
---

* Can only use lower 8 bits for requestCode
```
Caused by: java.lang.IllegalArgumentException: Can only use lower 8 bits for requestCode
at android.support.v4.app.FragmentActivity.requestPermissionsFromFragment(FragmentActivity.java:963)
at android.support.v4.app.FragmentActivity.access$000(FragmentActivity.java:80)
at android.support.v4.app.FragmentActivity$HostCallbacks.onRequestPermissionsFromFragment(FragmentActivity.java:1014)
at android.support.v4.app.Fragment.requestPermissions(Fragment.java:1031)
```
> 解决方法
> android 6.0 requestCode只能使用低8位，2的8次方即0-255之间的值

* Can only use lower 16 bits for requestCode
```
```
> 解决方法
> android 8.0 requestCode只能使用低16位，2的16次方即0-65536之间的值

### android 遇到问题已经解决的方案
```
# 如何在Activity/Fragment结束时处理异步回调？
* [1.0](http://iluhcm.com/2017/03/05/handle-asynchronous-callbacks-when-activity-finishes/)
* [1.1](https://easytoforget.github.io/2017/07/25/handle-callback-while-activity-or-fragment-finished/)
* [1.2](https://github.com/EasyToForget/LifefulDemo)
* [1.2](https://github.com/EasyToForget/LifefulDemo)

# Android Fragment 的使用，一些你不可不知的注意事项
* [1.0](http://yifeng.studio/2016/12/15/android-fragment-attentions/)

# 如何在回调时判断Activity，Fragment，ImageView等等是否已经被关闭
* [1.0](http://note.tyz.ren/blog/post/zerozhiqin/%E5%A6%82%E4%BD%95%E5%9C%A8%E5%9B%9E%E8%B0%83%E6%97%B6%E5%88%A4%E6%96%ADActivity%EF%BC%8CFragment%EF%BC%8CImageView%E7%AD%89%E7%AD%89%E6%98%AF%E5%90%A6%E5%B7%B2%E7%BB%8F%E8%A2%AB%E5%85%B3%E9%97%AD)
```

### 参考文章
