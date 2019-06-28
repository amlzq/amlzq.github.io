---
layout: post
title:  "Android AAPT命令"
date:   2018-05-25 17:00 +0800
categories: jekyll update
---
# 使用 aapt 命令
* 分析apk信息
>aapt l[ist] [-v] [-a] file.{zip,jar,apk}
>-v 以table形式列出来
>-a 详细列出内容

* 具体命令
>aapt dump badging xxx.apk
>aapt l[ist]:列出资源压缩包里的内容
>aapt d[ump]：查看APK包内指定的内容
aapt d[ump] [--values] WHAT file.{apk} [asset [asset ...]]
badging          Print the label and icon for the app declared in APK
permissions      Print the permissions from the APK.
resources        Print the resource table from the APK.
configurations   Print the configurations in the APK.
xmltree          Print the compiled xmls in the given assets.
xmlstrings       Print the strings of the given compiled xml assets.

>aapt p[ackage]：打包生成资源压缩包
>aapt r[emove]：从压缩包中删除指定文件
>aapt a[dd]：向压缩包中添加指定文件
>aapt v[ersion]:打印aapt的版本

bash clearAppData.sh com.droidyue.akoi
```

# 参考文章
* debug路径: C:/Users/%USERPROFILE%/.android/debug.keystore
* [Authenticating Your Client][Authenticating_Your_Client]

[Authenticating_Your_Client]: https://developers.google.com/android/guides/client-auth?hl=zh-cn

- 批量获取包名信息
- [https://www.jianshu.com/p/da0aee670ec7](https://www.jianshu.com/p/da0aee670ec7)
```
chcp 65001
REM  Copyrights: youngpen
REM  version:1.0
title 批量提取apk包名和应用名
rem 获取所有apk文件，使用aapt获得apk信息所在行
for /f "delims=" %%a in ('dir /b *.apk') do (
echo %%a >>temp_info.txt
aapt dump badging %%a |find "application-label:" >>temp_info.txt
aapt dump badging %%a |find "package:"  >>temp_info.txt
)
rem 将apk安装后的应用名和包名单独打印
for /f "tokens=2 delims='" %%i in ('find /i ":" temp_info.txt') do (
echo %%i >>result.txt
)
rem 删除临时文件
del temp_info.txt
echo 任务完成，点击任意键退出
exit
```

- [获取apk应用所有详细信息，python实现](https://github.com/poorevil/GetAPKDetails)
```

```