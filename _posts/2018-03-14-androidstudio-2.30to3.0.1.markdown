
# AndroidStudio 2.3.0 Upgrade 3.0.1

### 问题1
* 报错信息
```
Cannot set the value of read-only property 'outputFile' for ApkVariantOutputImpl_Decorated{apkData=Main{type=MAIN, fullName=debug, filters=[]}} of type com.android.build.gradle.internal.api.ApkVariantOutputImpl. Open File
```
* 解决方法
> 将2.3.0/3.3
```
	applicationVariants.all { variant ->
        variant.outputs.each { output ->
            def outputFile = output.outputFile
            if (outputFile != null && outputFile.name.endsWith('.apk')) {
                // 包名称-渠道名-版本号-版本名称-编译时间.apk
                def fileName = "${defaultConfig.applicationId}-${variant.productFlavors[0].name}-${variant.productFlavors[0].versionCode}-${variant.productFlavors[0].versionName}-${releaseTime()}.apk"
                output.outputFile = new File(outputFile.parent, fileName)
            }
        }
    }
```
> 改为3.0.1/4.1
```
	android.applicationVariants.all { variant ->
        variant.outputs.all { output ->
            def outputFile = output.outputFile
            if (outputFile != null && outputFile.name.endsWith('.apk')) {
                // 包名称-渠道名称-版本名称-编译时间.apk
                def fileName = outputFile.name.replace("app",
                        "${defaultConfig.applicationId}_${defaultConfig.name}-${variant.productFlavors[0].versionName}-${releaseTime()}")
                outputFileName = fileName
            }
        }
    }
```

### 问题2
* 
> 报错信息
```
Error:All flavors must now belong to a named flavor dimension. Learn more at https://d.android.com/r/tools/flavorDimensions-missing-error-message.html
```
* 解决方法
> app/build.gradle/android/defaultConfig里添加
```
flavorDimensions "versionCode"
```