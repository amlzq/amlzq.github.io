---
layout: post
title:  "AndroidStudio配置本地Maven仓库"
date:   2018-09-20 10:00
categories: jekyll update
---

### 参考文章
- [发布Android studio项目到本地Maven仓库](https://www.jianshu.com/p/8d7d0cc8fcc3)
- [Android studio中使用Maven发布本地仓库](https://www.jianshu.com/p/cff4684803f3)

### 实践
- 配置Module(apply plugin: 'com.android.library')的build.gradle
```
// 以下是发布到本地 maven 仓库配置
apply plugin: 'maven'

// 获取local.properties的内容
Properties properties = new Properties()
properties.load(project.rootProject.file('local.properties').newDataInputStream())

uploadArchives {
    repositories.mavenDeployer {
        repository(url: properties.getProperty("mavenLocal"))
        pom.groupId = "com.amlzq.android"
        pom.artifactId = "utils"
        pom.version = android.defaultConfig.versionName
    }
}
```
- 配置本地Maven地址
```
mavenLocal=file://C\:\\Users\\Administrator\\.m2\\repository
```
- 执行命令
```
gradlew uploadArchives
...
BUILD SUCCESSFUL
```
- 打包后输出文件
![]({{ site.baseurl }}/assets/android_studio_maven_local/result.png)
![]({{ site.baseurl }}/assets/android_studio_maven_local/result_2.png)