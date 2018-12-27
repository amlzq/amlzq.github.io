---
layout: post
title:  "Android Studio配置本地aar包依赖"
date:   2018-11-12 10:00
categories: jekyll update
---

### AS 2.3 / Gralde 3.3
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

### AS 3.0 / Gralde 4.1
- 
```
compile files('libs/toutiao-applog.aar')
```

### AS 3.2 / Gralde 4.6
- 
```
dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar', '*.aar'])
    ...
}
```