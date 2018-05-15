---
layout: post
title:  "AndroidStudio 2.3.0 Upgrade 3.0.1"
date:   2018-03-14 12:06:00 +0800
categories: jekyll update
---
### 问题1
* 报错信息
```
Cannot set the value of read-only property 'outputFile' for ApkVariantOutputImpl_Decorated{apkData=Main{type=MAIN, fullName=tencentx5Debug, filters=[]}} of type com.android.build.gradle.internal.api.ApkVariantOutputImpl. Open File
```
* 解决方法
> 将
```
applicationVariants.all { variant ->
    variant.outputs.each { output ->
        def outputFile = output.outputFile
        if (outputFile != null && outputFile.name.endsWith('.apk')) {
            // apk_渠道名-版本号-版本名称-编译时间.apk
            def fileName = "h5${appAbbreviation}.apk"
            output.outputFile = new File(outputFile.parent, fileName)
        }
    }
}
```
> 改为
```
android.applicationVariants.all { variant ->
    variant.outputs.all {
        // apk_渠道名-版本号-版本名称-编译时间.apk
        outputFileName = "h5${appAbbreviation}.apk"
    }
}
```

### 问题2
* 报错信息
> 
```
Error:All flavors must now belong to a named flavor dimension. Learn more at https://d.android.com/r/tools/flavorDimensions-missing-error-message.html
```
* 解决方法
> app/build.gradle/android/defaultConfig里添加
```
flavorDimensions "versionCode"
```