---
layout: post
title:  "Android Studio导入项目"
date:   2017-08-12 12:00 +0800
categories: jekyll update
---

`项目先不要急着导入，按如下操作后再导入，项目可以快速运行起来`
`步骤如下`

* 第一个文件:project-master\build.gradle

> 改为Android Plugin Version为本地版本
```
...
dependencies {
    classpath 'com.android.tools.build:gradle:3.0.1'

    // NOTE: Do not place your application dependencies here; they belong
    // in the individual module build.gradle files
}
...
```
> 增加Google's Maven，可更新android.support库
```
...
allprojects {
    repositories {
        jcenter()
        mavenCentral()
        google()
        // If you're using a version of Gradle lower than 4.1, you must instead use:
        // maven { url "https://maven.google.com" }
        // An alternative URL is 'https://dl.google.com/dl/android/maven2/'
    }
    gradle.projectsEvaluated { // 显示打包错误的详细信息
        tasks.withType(JavaCompile) {
            options.compilerArgs << "-Xlint:unchecked" << "-Xlint:deprecation"
        }
    }
}
...
```
> 增加统一依赖库版本（可选）
```
...
// Define versions in a single place
ext {
    // Sdk and tools
    minSdkVersion = 15
    targetSdkVersion = 27
    compileSdkVersion = 27
    buildToolsVersion = '27.0.3'

    // App dependencies
    supportLibraryVersion = '27.1.0'
    guavaVersion = '18.0'
    junitVersion = '4.12'
    mockitoVersion = '1.10.19'
    powerMockito = '1.6.2'
    hamcrestVersion = '1.3'
    runnerVersion = '1.0.1'
    rulesVersion = '0.5'
    espressoVersion = '3.0.1'
}
...
```

* 第二个文件:project-master\gradle\wrapper\gradle-wrapper.properties
> 修改gradle为本地版本
```
#Tue Jul 11 18:37:28 CST 2017
distributionBase=GRADLE_USER_HOME
distributionPath=wrapper/dists
zipStoreBase=GRADLE_USER_HOME
zipStorePath=wrapper/dists
distributionUrl=https\://services.gradle.org/distributions/gradle-4.1-all.zip
```

* 第三个文件:project-master\app\build.gradle
> 修改编译版本和构建工具版本
```
...
android {
    compileSdkVersion rootProject.ext.compileSdkVersion
    buildToolsVersion rootProject.ext.buildToolsVersion
    defaultConfig {
        minSdkVersion rootProject.ext.minSdkVersion
        targetSdkVersion rootProject.ext.targetSdkVersion
    }
}
...
```
> 修改依赖库版本
```
...
dependencies {
    compile fileTree(include: ['*.jar'], dir: 'libs')
    androidTestCompile("com.android.support.test.espresso:espresso-core:$rootProject.espressoVersion", {
        exclude group: 'com.android.support', module: 'support-annotations'
    })
    // Dependencies for local unit tests
    testCompile "junit:junit:$rootProject.ext.junitVersion"

    // App's dependencies, including test
    compile "com.android.support:appcompat-v7:$rootProject.supportLibraryVersion"
}
...
```
> 其他模块也一样修改:project-master\<other modules>\build.gradle

* 第四处文件:project-master\local.properties
> 修改SDK和NDK为本地路径
```
...
ndk.dir=C\:\\Android\\sdk\\ndk-bundle
sdk.dir=C\:\\Android\\sdk
...
```
---
