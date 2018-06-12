---
layout: post
title:  "Android反编译"
date:   2018-01-11 16:15:35 +0800
categories: jekyll update
---
### 需求
* Android 反编译，修改资源，重新打包，安装
* 修改apk，如：icon，app_name，string等等

#### 环境
* 安装[JDK][JDK-Install-Instructions]
> 详细请看官网
* 安装[Android SDK][AndroidSDK-Install-Instructions]
> 详细请看官网
* 安装[Apktool][Apktool-Install-Instructions]
> ![]({{ site.baseurl }}/assets/android_decompile/apktool_path.png)
> ![]({{ site.baseurl }}/assets/android_decompile/apktool_content.png)
* 增加APKTOOL_HOME系统变量
> ![]({{ site.baseurl }}/assets/android_decompile/apktool_sys_environment.png)
* 加入PATH系统变量
> ![]({{ site.baseurl }}/assets/android_decompile/apktool_path_environment.png)

#### 打开CMD.exe
> 可在任意路径执行以下命令

* 卸载
> adb uninstall [package name]

* 拆包
> apktool d [apk path]

* 修改
> icon <br>
> app name <br>
> smali <br>
> assets <br>

* 打包
> 删除apkname/build文件夹 <br>
> apktool b [new_apk path]

* 签名
```
jarsigner -digestalg SHA1 -sigalg MD5withRSA -verbose -keystore [keystore path] -signedjar [signed_apk path] [new_apk path] [your_key_store_alias]
```

* 对齐
> zipalign -v 4 [signed_apk path] [aligned_apk path]

* 安装
> adb install [aligned_apk path]

* 继续修改后重新打包
> 删除apkname/build文件夹

#### 更换apktool版本
* 需要删除这个文件`C:\Users\Administrator\apktool\framework\1.apk`

## 参考文章
* [Android开发中常用的命令总结](https://www.jianshu.com/p/58a23804da71)
* [签署您的应用](https://developer.android.com/studio/publish/app-signing#generate-key)
* [获取Android SHA1 、生成jks密钥、签名Apk](https://www.jianshu.com/p/692ca2bcbac5)


[JDK-Install-Instructions]: http://www.oracle.com/technetwork/java/javase/downloads/index.html
[AndroidSDK-Install-Instructions]: https://developer.android.com/index.html
[Apktool-Install-Instructions]: https://ibotpeaches.github.io/Apktool/install/

[Apktool]: https://ibotpeaches.github.io/Apktool/