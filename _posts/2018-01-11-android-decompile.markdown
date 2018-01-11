---
layout: post
title:  "Android Decompile"
date:   2017-07-16 13:37:35 +0800
categories: jekyll update
---
### Android 反编译，修改资源，重新打包，安装
* 需求是修改一个apk的内容，如：icon，app_name，string等等

###### 环境
* 安装[JDK][JDK-Install-Instructions]
> 详细请看官网
* 安装[Android SDK][AndroidSDK-Install-Instructions]
> 详细请看官网
* 安装[Apktool][Apktool-Install-Instructions]
> ![](res\android-decompile\android_decompile\apktool_path.png)
> ![](res\android-decompile\android_decompile\apktool_content.png)
* 增加APKTOOL_HOME系统变量
> ![](res\android-decompile\android_decompile\apktool_sys_environment.png)
* 加入PATH系统变量
> ![](res\android-decompile\android_decompile\apktool_path_environment.png)

###### 打开CMD.exe
> 在任意路径执行以下命令

* 卸载
> adb uninstall [package name]

* 拆包
> apktool d [apk path]

* 修改
> icon
> app name
> smali
> assets

* 打包
> 删除apkname/build文件夹
> apktool b [new_apk path]

* 签名
> jarsigner -digestalg SHA1 -sigalg MD5withRSA -verbose -keystore [keystore path] -signedjar [signed_apk path] [new_apk path] [Alias]

* 对齐
> zipalign 4 [signed_apk path] [aligned_apk path]

* 安装
> adb install [aligned_apk path]

###### 更换apktool版本
* 需要删除这个文件`C:\Users\Administrator\apktool\framework\1.apk`

[JDK-Install-Instructions]: http://www.oracle.com/technetwork/java/javase/downloads/index.html
[AndroidSDK-Install-Instructions]: https://developer.android.com/index.html
[Apktool-Install-Instructions]: https://ibotpeaches.github.io/Apktool/install/
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/