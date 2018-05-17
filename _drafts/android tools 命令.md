
# 使用adb命令

## 第一步

* 配置环境变量 Android adb aapt命令
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

# 使用aapt命令
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

## 创建证书
* keytool -genkeypair -alias "test" -keyalg "RSA" -keystore <keystore path>

## 查看keystore的信息
* keytool -list -v -keystore <keystore path>
* keytool -exportcert -keystore <keystore path> -list -v
* keytool -list -keystore <keystore path>

## 查看APK证书信息
* keytool -printcert -file <META-INF/CERT.RSA PATH>

## 查看文件的MD5值
* certutil -hashfile <filepath> MD5
* certutil -hashfile <filepath> SHA1
* certutil -hashfile <filepath> SHA256

## 加固后再签名
* jarsigner -digestalg SHA1 -sigalg MD5withRSA -verbose -keystore [your_key_store_path] -signedjar [signed_apk_path] [usigned_apk_path] [your_key_store_alias]

## 查看设备当前的activity
* adb shell dumpsys activity top

## log
* adb shell setprop log.tag.Main V

## 
* adb shell pm clear <package name>

## 常用的package name
* google play
> com.android.vending

## 获取当前


##
* release to gist

## 参考文章
* [Android开发中常用的命令总结](https://www.jianshu.com/p/58a23804da71)
