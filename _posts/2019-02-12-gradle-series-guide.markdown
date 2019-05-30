---
layout: post
title:  "Gradle指南"
date:   2018-05-01 19:00 +0800
categories: jekyll update
---

- 这是一篇指南，引导，汇总的文章
- 按索引直接获取帮助

### Android Studio Gradle



- 配置签名
	```
		// 测试证书举例：
		signingConfigs {
	        release {
	            keyAlias 'androiddebugkey'
	            keyPassword 'android'
	            storeFile file("C:/Users/${USER}/.android/debug.keystore")
	            storePassword 'android'
	            v1SigningEnabled true
	            v2SigningEnabled false
	        }
	        debug {
	            keyAlias 'androiddebugkey'
	            keyPassword 'android'
	            storeFile file("C:/Users/${USER}/.android/debug.keystore")
	            storePassword 'android'
	            v1SigningEnabled true
	            v2SigningEnabled false
	        }
	    }
	    ...
	    buildTypes {
	        debug {
	        	...
	            signingConfig signingConfigs.debug
	        }
	        release {
	            ...
	            signingConfig signingConfigs.release
	        }
    	}
	```

### 实践
- 
- 
- 
