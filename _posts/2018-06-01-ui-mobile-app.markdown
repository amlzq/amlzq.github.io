---
layout: post
title:  "移动APPUI设计规范"
date:   2018-06-01 00:00 +0800
categories: jekyll update
---

- 本文使用[Markdown](http://wowubuntu.com/markdown/)编写

* ARGB 中的透明度alpha，表示的是不透明度。

| 不透明度 | 16进制表示 |
| -------------- | -------------- |
| 100% | 00 |
| 95% | 0D |
| 90% | 1A |
| 85% | 26 |
| 80% | 33 |
| 75% | 40 |
| 70% | 4D |
| 65% | 59 |
| 60% | 66 |
| 55% | 73 |
| 50% | 80 |
| 45% | 8C |
| 40% | 99 |
| 35% | A6 |
| 30% | B3 |
| 25% | BF |
| 20% | CC |
| 15% | D9 |
| 10% | E6 |
| 5% | F2 |
| 0% | FF |

- [Android 颜色透明度换算](http://www.snowdream.tech/2016/03/11/android-color-argb-alpha-convert/)

### APP UI设计规范
- [规范](http://www.zcool.com.cn/work/ZMTI0MTc3NDg=.html)
- [Material Design](http://design.1sters.com/material_design/material-design/introduction.html)
- [APP设计规范](http://www.jianshu.com/p/a2a4c18c1900)
- [移动端UI设计规范-第一谈Android系统](http://www.zcool.com.cn/work/ZMTkxOTM3NzY=.html)
- [Android手机UI界面设计常用规范](http://www.zcool.com.cn/work/ZMTI0MTc3NDg=.html)
- IOS和Android规范，UI看什么？系列
- [IOS和Android规范，UI看什么？（一）](http://old.zcool.com.cn/article/ZNDk2NTQw.html)
- [IOS和Android规范，UI看什么？（二）](http://old.zcool.com.cn/article/ZNDk4NDQ4.html)
- [IOS和Android规范，UI看什么？（三）](http://old.zcool.com.cn/article/ZNDk5Mjcy.html)

### ICON
* [设计规范1](https://developer.android.com/guide/practices/ui_guidelines/icon_design)
* [设计规范2](https://material.io/design/iconography/product-icons.html#)
* [设计规范3](https://www.jianshu.com/p/7a238062129a)
* [小米特殊要求1](https://dev.mi.com/console/doc/detail?pId=1162)
* [小米特殊要求2](https://dev.mi.com/doc/p=204/index.html)
- [iOS和安卓APP启动图标的尺寸和圆角大小详解](https://www.25xt.com/iconweb/11704.htm)
- [APP图标尺寸](https://www.jianshu.com/p/d6be2dc801e9)
- [App常用图标尺寸规范汇总](https://likfe.com/2016/07/26/android-size-set/)

### 设计

#### 设计实践
- [IOS切图直接作为Android切图使用](https://blog.csdn.net/ecjtuhq/article/details/52204599)
- [如何一稿适配 iOS、Android](https://zhuanlan.zhihu.com/p/22084291)

- 要求
```
	1.按主流的 1280*720 分辨率设计

	2.按钮交互状态

	3.出图格式：
		图标 .png
		大的背景 .jpg
		九宫图	.9.png
		纯色图	不用出图，程序实现

	4.效果图请标注
		颜色可以省略不标
		尺寸一定要标注（字体大小和间距）
```

### 出图

#### 图片命名
* 

#### 尺寸换算
- [iOS和android布局开发单位对比(pt VS dp)](https://juejin.im/entry/5a37bd866fb9a04509099d25)

#### SVG
- [添加多密度矢量图形](https://developer.android.com/studio/write/vector-asset-studio?hl=zh-cn)
- 设计师输出png图片，通过上传iconfont官网后再下载使用
```
https://andyliwr.github.io/2018/01/10/ps_cutterman/
```
- 设计师输出png图片，通过上传iconfont官网后再下载使用

### iOS UI

### Android UI
* 表格
| 密度 | 密度值 | 分辨率 |
| -------------- | -------------- | -------------- |
| ldpi | 120 | 240x320 |
| mdpi | 160 | 320x480 |
| hdpi | 240 | 480x800 |
| xhdpi | 320 | 720x1280 |
| xxhdpi | 480 | 1080x1920 |
| xxxhdpi | 960 | 1440x2560 |

- android系统字体
- [安卓系统的默认中文字体](https://www.zhihu.com/question/23487706)

* 设计时，用1080*1920的设计稿进行设计
* 切图时，切xhdpi，xxhdpi的图标，图片为PNG格式，xxhdpi的banner等位图，大幅的背景图出jpg格式。
* 标注时，距离用dp，字号用sp

- [Android UI 设计规范](https://www.jianshu.com/p/b38e81be51ca)
- [追随Google的脚步，知乎安卓客户端Material Design实战规范！](http://www.tuyiyi.com/v/40056.html)

