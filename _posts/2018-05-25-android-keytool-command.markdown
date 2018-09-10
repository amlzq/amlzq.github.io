---
layout: post
title:  "Android keytool命令"
date:   2018-05-25 19:00 +0800
categories: jekyll update
---

### 本机环境
* windows 7
* 工具路径
```
C:\Program Files\Java\jdk1.8.0_25\bin\keytool.exe
```

* 打开CMD，输入keytool，查看命令列表
```
C:\Users\%USERPROFILE%>keytool
密钥和证书管理工具

命令:

 -certreq            生成证书请求
 -changealias        更改条目的别名
 -delete             删除条目
 -exportcert         导出证书
 -genkeypair         生成密钥对
 -genseckey          生成密钥
 -gencert            根据证书请求生成证书
 -importcert         导入证书或证书链
 -importpass         导入口令
 -importkeystore     从其他密钥库导入一个或所有条目
 -keypasswd          更改条目的密钥口令
 -list               列出密钥库中的条目
 -printcert          打印证书内容
 -printcertreq       打印证书请求的内容
 -printcrl           打印 CRL 文件的内容
 -storepasswd        更改密钥库的存储口令
 -validity           有效期天数

使用 "keytool -command_name -help" 获取 command_name 的用法
```

### 常用业务

* 生成证书，这里以jdk1.7版本为例，jdk1.8和jdk1.7的算法有所不同
```
keytool -genkeypair -alias <alias> -keyalg RSA -validity 20000 -keystore <keystore file path>
样例:
keytool -genkeypair -alias "amlzq" -keyalg RSA -validity 20000 -keystore C:\Users\%USERPROFILE%\android\appName.keystore
```

* 手动生成签名证书
```
文件名: filename.keystore
keyStore Password: 
Alias: 
Password: 
Validity(years): 50

First and Last Name(): 
Organizational Unit(组织单位名称): 深圳游禧科技有限公司
Organizational(组织名称): 深圳游禧科技有限公司
City or Locality(城市或区域名称): 深圳市
State or Province(省市): 广东省
Country Code(国家、地区代码): CN
```

* 列出密钥库中的条目
```
keytool -list -v -keystore <keystore path>			详细
keytool -list -keystore <keystore path>				简单
```
```
样例:
C:\Users\%USERPROFILE%>keytool -list -v -keystore C:\Users\%USERPROFILE%\.android\debug.keystore
输入密钥库口令: android

密钥库类型: JKS
密钥库提供方: SUN

您的密钥库包含 1 个条目

别名: androiddebugkey
创建日期: 2016-4-8
条目类型: PrivateKeyEntry
证书链长度: 1
证书[1]:
所有者: CN=Android Debug, O=Android, C=US
发布者: CN=Android Debug, O=Android, C=US
序列号: 75c76b4d
有效期开始日期: Fri Apr 08 15:03:55 CST 2016, 截止日期: Sun Apr 01 15:03:55 CST 2046
证书指纹:
         MD5: D1:91:78:57:57:FD:45:42:C0:FE:DD:7C:E0:A2:DD:26
         SHA1: 6E:1A:9A:60:20:26:22:1D:DB:03:0A:5E:9E:BB:F6:57:9F:A0:23:61
         SHA256: AC:30:C8:63:B7:90:5D:BF:64:28:0D:9B:EE:83:09:7A:AB:AD:44:69:CC:91:4D:11:71:67:41:3A:14:B1:98:78
         签名算法名称: SHA256withRSA
         版本: 3

扩展:

#1: ObjectId: 2.5.29.14 Criticality=false
SubjectKeyIdentifier [
KeyIdentifier [
0000: 61 26 31 CA EA 07 A8 A6   1F 7F 41 BE 26 64 97 EB  a&1.......A.&d..
0010: A7 EA D9 47                                        ...G
]
]



*******************************************
*******************************************
```

* 导出证书
```
keytool -exportcert -keystore <keystore path> -list -v
// To get the release certificate fingerprint:
keytool -exportcert -list -v -alias <your-key-name> -keystore <path-to-production-keystore>
// To get the debug certificate fingerprint:
keytool -exportcert -list -v -alias androiddebugkey -keystore %USERPROFILE%\.android\debug.keystore
```

* 通过APK查看签名证书，解压apk文件
```
keytool -printcert -file <META-INF/CERT.RSA PATH>
```

### 参考文章
* debug路径: C:/Users/%USERPROFILE%/.android/debug.keystore
* [Authenticating Your Client][Authenticating_Your_Client]

[Authenticating_Your_Client]: https://developers.google.com/android/guides/client-auth?hl=zh-cn