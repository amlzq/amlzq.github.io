---
layout: post
title:  "Android Gradle"
date:   2018-06-04 10:00 +0800
categories: jekyll update
---

所以我们需要在这个compile中增加exclude, 把google的广告模块去掉,如下:
compile ('com.facebook.android:audience-network-sdk:4.8.2'){
            exclude module: 'play-services-ads'
}

平时如何查看一个依赖是否包含了其他依赖呢? 使用如下命令:
./gradlew -q app:dependencies
app表示你自己的module的名称,可自行修改

自定义混淆规则文件的路径
buildTypes {  
        debug {  
            minifyEnabled false  
        }  
  
        release {  
            minifyEnabled true  
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro', "../submodule/proguard-rules.pro"  
            signingConfig signingConfigs.release  
        }  
    }  


// gradlew -q dependencies app:dependencies --configuration comp
// 查看support libraries must use the exact same version specification问题


sourceSets {
        main {
            manifest.srcFile 'src/main/AndroidManifest.xml'
            java.srcDirs = ['src/main/java']
            resources.srcDirs = ['src/main/resources']
            aidl.srcDirs = ['src/main/aidl']
            renderscript.srcDirs = ['src/maom']
            res.srcDirs = ['src/main/res']
            assets.srcDirs = ['src/main/assets']
            jniLibs.srcDir 'src/main/jniLibs'
        }
        hybrid {
            manifest.srcFile 'src/hybrid/AndroidManifest.xml'
            java.srcDirs = ['src/hybrid/java']
            resources.srcDirs = ['src/hybrid/resources']
            aidl.srcDirs = ['src/hybrid/aidl']
            renderscript.srcDirs = ['src/maom']
            res.srcDirs = ['src/hybrid/res']
            assets.srcDirs = ['src/hybrid/assets']
            jniLibs.srcDir 'src/hybrid/jniLibs'
        }
        web {
            manifest.srcFile 'src/web/AndroidManifest.xml'
            java.srcDirs = ['src/web/java']
            resources.srcDirs = ['src/web/resources']
            aidl.srcDirs = ['src/web/aidl']
            renderscript.srcDirs = ['src/maom']
            res.srcDirs = ['src/web/res']
            assets.srcDirs = ['src/web/assets']
            jniLibs.srcDir 'src/web/jniLibs'
        }
    }

- [Android Gradle进阶配置指南](https://juejin.im/post/5be97882e51d4502df234ee4)

- 加@aar与不加的区别
```
首先这是指定格式，@aar或者@jar
其次会丢失传递依赖
有些lib不支持@jar，比如：com.android.support:appcompat-v7
```
- [Why should I include a gradle dependency as `@aar`](https://stackoverflow.com/questions/30157575/why-should-i-include-a-gradle-dependency-as-aar)