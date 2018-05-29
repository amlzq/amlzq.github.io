---
layout: post
title:  "Windows CMD命令"
date:   2018-04-26 17:00 +0800
categories: jekyll update
---
* 查看文件属性
```
certutil -hashfile <file path> MD5
certutil -hashfile <file path> SHA1
certutil -hashfile <file path> SHA256
```

* Windows7/环境变量/系统变量/Path/Value
```
%RUBY_HOME%\bin;C:\ProgramData\Oracle\Java\javapath;C:\Program Files (x86)\Intel\iCLS Client\;C:\Program Files\Intel\iCLS Client\;%SystemRoot%\system32;%SystemRoot%;%SystemRoot%\System32\Wbem;%SYSTEMROOT%\System32\WindowsPowerShell\v1.0\;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\IPT;C:\Program Files\Intel\Intel(R) Management Engine Components\IPT;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;C:\Program Files\Git\cmd;C:\Program Files\TortoiseGit\bin;C:\Program Files (x86)\GtkSharp\2.12\bin;%USERPROFILE%\.dnx\bin;C:\Program Files\Microsoft DNX\Dnvm\;C:\Program Files\Microsoft SQL Server\130\Tools\Binn\;C:\Program Files (x86)\Windows Kits\8.1\Windows Performance Toolkit\;D:\Program Files\Binaries-LuaDist-batteries-0.9.8-Windows-x86\bin;%PYTHON_HOME%;%android%;%GRADLE_HOME%\bin;%APKTOOL_HOME%
```
---

# 参考文章
* debug路径: C:/Users/%USERPROFILE%/.android/debug.keystore
* [Authenticating Your Client][Authenticating_Your_Client]

[Authenticating_Your_Client]: https://developers.google.com/android/guides/client-auth?hl=zh-cn