---
layout: post
title:  "AndroidStudio 2.3.0升级3.0.1"
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

### 问题3
* 报错信息
>  
```
Error:Resource shrinker cannot be used for libraries.
library中不要使用移除无用的资源文件字段
```
* 解决方式
> shrinkResources false // 移除无用的resource文件

### 问题4
* 报错信息
> 
```
Error:All flavors must now belong to a named flavor dimension. Learn more at https://d.android.com/r/tools/flavorDimensions-missing-error-message.html
```
* 解决方式
> 

### Unable to load class 'org.gradle.api.internal.component.Usage'.
* 报错信息
> 
```
Unable to load class 'org.gradle.api.internal.component.Usage'. Possible causes for this unexpected error include:
Gradle's dependency cache may be corrupt (this sometimes occurs after a network connection timeout.) Re-download dependencies and sync project (requires network)
The state of a Gradle build process (daemon) may be corrupt. Stopping all Gradle daemons may solve this problem. Stop Gradle build processes (requires restart)
Your project may be using a third-party plugin which is not compatible with the other plugins in the project or the version of Gradle requested by the project.
In the case of corrupt Gradle processes, you can also try closing the IDE and then killing all Java processes.
```
* [解决方式](https://www.jianshu.com/p/25d9db6d61f4)

### 参考文章
* [迁移到 Android Plugin for Gradle 3.0.0](https://developer.android.com/studio/build/gradle-plugin-3-0-0-migration)
* [个人总结：AS升级到3.0后遇到的问题及解决方法](https://www.jianshu.com/p/02a62574d9a1)