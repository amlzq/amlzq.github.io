---
layout: post
title:  "配置本地aar包依赖"
date:   2019-02-12 10:00
categories: jekyll update
---

### 打包aar包


### 使用aar包

#### AS2.3 / Gralde3.3
- 在Project的build.gradle中配置
```
allprojects {
    repositories {
        ...
        // 本地aar
        flatDir {
            dirs 'libs'
        }
        ...
    }
}
```
- 在Module的build.gradle中配置 libs/*.aar
```
compile(name: 'aar_file_name', ext: 'aar')
```


#### AS3.0 / Gralde4.1
- 
```
compile files('libs/toutiao-applog.aar')
```

#### AS3.2 / Gralde4.6
- 
```
dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar', '*.aar'])
    ...
}
compileOnly
api/implementation
```
