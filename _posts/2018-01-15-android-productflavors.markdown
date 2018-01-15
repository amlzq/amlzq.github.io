---
layout: post
title:  "Android ProductFlavors"
date:   2018-01-15 21:03:00 +0800
categories: jekyll update
---
### Android 产品风味
* 需求是application module和library module不同市场渠道配置不同的资源

#### 环境
> [Android Studio][AndroidStudio-Install-Instructions] 版本:2.3
> [Gradle][Gradle-Install-Instructions] 版本:3.3

#### 配置Application Module
##### 在application module/build.gradle增加
	apply plugin: 'com.android.application'

	android {
		...
		publishNonDefault true //去除gradle对library module默认只编译release buildType的限制
		productFlavors {
		    chinese {
		    	applicationId "com.company.project.chinese"
		        versionCode 200
		        versionName "2.0.0"
		    }
		    global {
		    	applicationId "com.company.project.global"
		        versionCode 1
		        versionName "1.0.0"
		    }
		}
		...
		sourceSets {
			// defaultConfig
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
	        chinese {
	            manifest.srcFile 'src/chinese/AndroidManifest.xml'
	            java.srcDirs = ['src/chinese/java']
	            resources.srcDirs = ['src/chinese/resources']
	            aidl.srcDirs = ['src/chinese/aidl']
	            renderscript.srcDirs = ['src/maom']
	            res.srcDirs = ['src/chinese/res']
	            assets.srcDirs = ['src/chinese/assets']
	            jniLibs.srcDir 'src/chinese/jniLibs'
	        }
	        global {
	            manifest.srcFile 'src/global/AndroidManifest.xml'
	            java.srcDirs = ['src/global/java']
	            resources.srcDirs = ['src/global/resources']
	            aidl.srcDirs = ['src/global/aidl']
	            renderscript.srcDirs = ['src/maom']
	            res.srcDirs = ['src/global/res']
	            assets.srcDirs = ['src/global/assets']
	            jniLibs.srcDir 'src/global/jniLibs'
	        }
    	}
    	...
    	configurations {
    		chineseDebugCompile
    		globalDebugCompile
		}
		...
		// 依赖不同的library
		chineseDebugCompile project(path: ':sdk', configuration: 'chineseDebug')
    	globalDebugCompile project(path: ':sdk', configuration: 'globalDebug')
    	...
	}

#### Library Module配置
##### 创建library module/libs_chinese

##### 创建library module/libs_global

##### 在library module/build.gradle增加
	apply plugin: 'com.android.library'
	import java.util.regex.Matcher
	import java.util.regex.Pattern

	android {
		...
		publishNonDefault true //去除gradle对library module默认只编译release buildType的限制
		productFlavors {
		    chinese {
		        versionCode 200
		        versionName "2.0.0"
		    }
		    global {
		        versionCode 1
		        versionName "1.0.0"
		    }
		}
		...
		sourceSets {
			// defaultConfig
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
	        chinese {
	            manifest.srcFile 'src/chinese/AndroidManifest.xml'
	            java.srcDirs = ['src/chinese/java']
	            resources.srcDirs = ['src/chinese/resources']
	            aidl.srcDirs = ['src/chinese/aidl']
	            renderscript.srcDirs = ['src/maom']
	            res.srcDirs = ['src/chinese/res']
	            assets.srcDirs = ['src/chinese/assets']
	            jniLibs.srcDir 'src/chinese/jniLibs'
	        }
	        global {
	            manifest.srcFile 'src/global/AndroidManifest.xml'
	            java.srcDirs = ['src/global/java']
	            resources.srcDirs = ['src/global/resources']
	            aidl.srcDirs = ['src/global/aidl']
	            renderscript.srcDirs = ['src/maom']
	            res.srcDirs = ['src/global/res']
	            assets.srcDirs = ['src/global/assets']
	            jniLibs.srcDir 'src/global/jniLibs'
	        }
    	}
    	...
    	def buildLibs() {
		    String currentFlavor = getCurrentFlavor()
		    println("current Flavor:" + currentFlavor)
		    boolean isChinese = "chinese".equalsIgnoreCase(currentFlavor)
		    println("is Chinese Flavor:" + isChinese)
		    if (isChinese) {
		        return 'libs_chinese'
		    }
		    return 'libs'
		}
		...
		def getCurrentFlavor() {
		    String taskRequestName = getGradle().getStartParameter().getTaskRequests().toString()
		    Pattern pattern;
		    if (taskRequestName.contains("assemble"))
		        pattern = Pattern.compile("assemble(\\w+)(Release|Debug)")
		    else
		        pattern = Pattern.compile("generate(\\w+)(Release|Debug)")
		    Matcher matcher = pattern.matcher(taskRequestName)
		    if (matcher.find()) {
		        return matcher.group(1).toLowerCase()
		    } else {
		        return "";
		    }
		}
	}

#### 参考文章
* [官方文档][build-variants-instructions]
* [Product Flavors for Android Library](https://android.jlelse.eu/product-flavors-for-android-library-d3b2d240fca2)
* [Android Studio多渠道打包](https://www.ezlippi.com/blog/2015/03/android-studio-prefrence.html)
* [Android studio gradle中分渠道加载res、libraries及Class](https://www.jianshu.com/p/d7d51a1363cd)
* [Android Studio Gradle实践之多渠道自动化打包+版本号管理](https://unclechen.github.io/2015/10/22/Android%20Studio%20Gradle%E5%AE%9E%E8%B7%B5%E4%B9%8B%E5%A4%9A%E6%B8%A0%E9%81%93%E8%87%AA%E5%8A%A8%E5%8C%96%E6%89%93%E5%8C%85+%E7%89%88%E6%9C%AC%E5%8F%B7%E7%AE%A1%E7%90%86/)

[AndroidStudio-Install-Instructions]: https://developer.android.com/studio/index.html
[Gradle-Install-Instructions]: https://gradle.org/
[build-variants-instructions]: https://developer.android.com/studio/build/build-variants.html?hl=zh-cn