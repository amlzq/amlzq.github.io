---
layout: post
title:  "Android Module注意事项"
date:   2018-08-06 00:00
categories: jekyll update
---

* 外部要引用Module/libs中的类库
> 一般Module/libs对于引用者来说是透明的，所以设置如下即可
```
dependencies {
	implementation fileTree(dir: 'libs', include: ['*.jar'])
	...
}
```
> 但是有些情况需要Module/libs，则按如下配置
```
dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    ...
}    
```