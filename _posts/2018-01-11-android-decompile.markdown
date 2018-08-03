---
layout: post
title:  "Android反编译"
date:   2018-01-11 16:15:35 +0800
categories: jekyll update
---
## 需求
* APK反编译，修改资源，重新打包，签名，对齐，安装

### 本地环境
* windows系统
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

### 步骤
* 打开CMD.exe
* 可在任意路径执行以下命令

#### 卸载
* 工具
> Android\sdk\platform-tools\adb.exe
* 命令
```
adb uninstall <package name>
```

#### 拆包
* 工具
> apktool.bat <br>
> apktool.jar <br>
* 命令
```
apktool d <apk path> -o <output path>
```

#### 修改
> AndroidManifest.xml <br>
> res <br>
> smali <br>
> assets <br>
> lib <br>

#### 打包
```
apktool b <file path> -o <new_apk path>
```

#### 签名
* 工具
> Java\jdk1.8.0_25\bin\jarsigner.exe
* 命令
```
jarsigner -digestalg SHA1 -sigalg MD5withRSA -verbose -keystore <keystore path> -signedjar <signed_apk path> <new_apk path> <your_key_store_alias>
输入签名证书密码: *******
```

#### zipalign和V2签名
* 工具
> 工具位于Android SDK/build-tools/SDK版本/zipalign.exe <br>
> zipalign 是对zip包对齐的工具,使APK包内未压缩的数据有序排列对齐,从而减少APP运行时内存消耗
* 命令
```
zipalign -v 4 <signed_apk path> <aligned_apk path>			//4字节对齐优化
zipalign -c -v 4 <aligned_apk path>        					//检查APK是否对齐
```
> zipalign可以在V1签名后执行 <br>
> 但zipalign不能在V2签名后执行,只能在V2签名之前执行

#### 安装
> adb install <aligned_apk path>

#### 继续修改后重新打包
> 删除反编译输出文件夹中的build文件夹

### 更换apktool版本
* 需要删除这个文件`C:\Users\Administrator\apktool\framework\1.apk`

### 常见问题
* 错误1
```
        at brut.util.OS.exec(OS.java:97)
        at brut.androlib.res.AndrolibResources.aaptPackage(AndrolibResources.java:430)
        ... 6 more
Caused by: java.io.IOException: Cannot run program "C:\Users\asus\AppData\Local\Temp\brut_util_Jar_1685061613003189837.t
mp": CreateProcess error=206, 文件名或扩展名太长。
        at java.lang.ProcessBuilder.start(Unknown Source)
        at brut.util.OS.exec(OS.java:90)
        ... 7 more
Caused by: java.io.IOException: CreateProcess error=206, 文件名或扩展名太长。
        at java.lang.ProcessImpl.create(Native Method)
        at java.lang.ProcessImpl.<init>(Unknown Source)
        at java.lang.ProcessImpl.start(Unknown Source)
        ... 9 more
```
* 解决方案
```
just run it on linux or OSX.

The simple solution:

edit the apktool.yml
set the doNotCompress to null
```
```
1.缩短项目文件的目录层级
2.拥抱Linux
```
> [Decompile An Apk success,But Recompile fail](https://github.com/iBotPeaches/Apktool/issues/1623)
> [CREATEPROCESS ERROR=206,文件名或扩展名太长](http://www.blackcat-tech.com/archives/740)
> [问题分析](https://www.jianshu.com/p/fed8a392c0a0)

* 错误2
```
Failure [INSTALL_FAILED_TEST_ONLY: installPackageLI]
```
* [解决方案1](https://blog.csdn.net/chf1142152101/article/details/70738868)
* [解决方案2](https://www.jianshu.com/p/8f5730cab8fc)

## 参考文章
* [Command line tools](https://developer.android.com/studio/command-line/?hl=zh-cn)
* [Android开发中常用的命令总结](https://www.jianshu.com/p/58a23804da71)
* [签署您的应用](https://developer.android.com/studio/publish/app-signing#generate-key)
* [获取Android SHA1 、生成jks密钥、签名Apk](https://www.jianshu.com/p/692ca2bcbac5)

[JDK-Install-Instructions]: http://www.oracle.com/technetwork/java/javase/downloads/index.html
[AndroidSDK-Install-Instructions]: https://developer.android.com/index.html
[Apktool-Install-Instructions]: https://ibotpeaches.github.io/Apktool/install/
[Apktool]: https://ibotpeaches.github.io/Apktool/