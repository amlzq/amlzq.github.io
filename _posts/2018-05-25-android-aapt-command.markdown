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