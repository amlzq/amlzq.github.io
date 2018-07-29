# _drafts文件夹说明文档

## 模板
```
---
layout: post
title:  "填写标题"
date:   1970-01-01 00:00 +0800
categories: jekyll update
---

### 正文

### 参考文章
* [文字说明][文字说明]

[文字说明]: 链接
```

## 需要理解的疑惑

### Java JDK的jre和Android Studio的jre区分和联系
* C:\Program Files\Java\jdk1.8.0_25\jre
* I:\Android\android-studio-ide-171.4443003-windows\android-studio\jre

## 做的比较好的Demo，有参考价值
* 网易七鱼Demo
* 当乐SDKDemo

## Android技术调研-定位服务
* [安卓定位及坐标转换](https://www.jianshu.com/p/ddc6141bac95)
* [原生API实现](http://blog.csdn.net/luosiye312/article/details/50562309)

### 查看apk包体信息
* 需要apk
* 通过Android DevTools应用查看
* 通过python脚本查看

### gms-play-services

### facebook-sdk

#### 

### Firebase
* 
* https://firebase.google.com/docs/auth/android/facebook-login?hl=zh-cn

### 

### Android技术调研-Data Binding
* 参考文章
[](https://segmentfault.com/a/1190000002876984#articleHeader5)
[]()

### Android技术调研-权限管理机制
* [Google API For Android](https://developers.google.com/android/)
* [AppOpsManager权限检测适配](https://www.jianshu.com/p/352c4b9d320d)

### 2018-05-11-Android DragLayout
* 可供拖动的布局

* LayoutInflater.from(mContext).inflate(R.layout.sdk7477_widget_floatmenu, null)
* 搞明白，这个参数的作用，草草草
* root Optional view to be the parent of the generated hierarchy.

* [可以在android实践的github项目中敲一遍](https://juejin.im/entry/58133085128fe100557e4579)


### Java 反射
* [一篇文章带你学懂Java反射-ming152](https://mp.weixin.qq.com/s?__biz=MzA5MzI3NjE2MA==&mid=2650242963&idx=1&sn=708e4fa01823b7844494ecb276a3733f&chksm=88638efcbf1407eaf0b5438f824a42a1890ab6a623108990cbbc1d424594ee08e9ff973ff70f&scene=0#rd)

### AS项目结构
项目含一个app src目录，4个测试目录，
分别是androidTest（UI层测试）、androidTestMock（UI层测试mock数据支持）、test（业务层单元测试）、mock（业务层单元测试mock数据支持）。src目录的代码组织方式完全是按照功能来组织的，功能内部分为xactivity、xcontract、xfragment、xpresenter四个类文件(x代表业务名称)。

### 泡椒网游戏SDK
* [Jianbo Peng](https://github.com/pengjianbo?tab=repositories)
> 

### 融合渠道SDK的技术分析
* [huanleyouren](https://github.com/huanleyouren)
* [QuickSDKTool_Win_P34](https://github.com/huanleyouren/QuickSDKTool_Win_P34)
* Fusion Game sdk 聚合游戏sdk

### 悬浮视图
* [泡椒网游戏SDK Float View(悬浮窗)](https://github.com/pengjianbo/FloatViewFinal)
* https://github.com/zhaozepeng/FloatWindowPermission

### CMDB
* [open-cmdb/cmdb](https://github.com/open-cmdb/cmdb)

### 热更新
dex分包方案

### 服务端返回的数据格式
```
1. data:[]
列表数据为空有两种情况
```

### android-support-base需求

#### utils
* [获取Manifest中<meta-data>元素的值](http://blog.csdn.net/zhanghao_hulk/article/details/8662917)
* [android-RuntimePermissions](https://github.com/googlesamples/android-RuntimePermissions)
* deviceUtil 获取 imsi/imei
* 系统分享功能
https://www.jianshu.com/p/88f166dd43b7
https://blog.csdn.net/zh_ang_lei/article/details/52385678
https://github.com/baishixian/Share2

#### net
* https://blog.csdn.net/hanqunfeng/article/details/4510338
```
jdk1.4换成这个,连接超时
System.setProperty("sun.NET.client.defaultConnectTimeout", "10000");
jdk1.4换成这个,读操作超时
System.setProperty("sun.net.client.defaultReadTimeout", "5000");
```
* 原声API类库适配HTTPS
> https://juejin.im/entry/575ab9b36be3ff0069492bc6

#### download
* Android多线程下载
* [Android多线程断点续传下载](https://www.jianshu.com/p/2b82db0a5181)
> Demo
* https://github.com/AigeStudio/MultiThreadDownloader
* https://github.com/Jerrywen/MultiThreadDownloader

* [MultiThreadDownloader下载库的使用详解](https://www.jianshu.com/p/af5c57ef3d8f)
> Demo https://github.com/Aspsine/MultiThreadDownload
> 靠谱

#### io
* xml解析数据，webgame项目中有部分代码可以抽取

#### ui
* 修改系统对话框的颜色
```
try {
            Field mAlert = AlertDialog.class.getDeclaredField("mAlert");
            mAlert.setAccessible(true);
            Object mAlertController = mAlert.get(dialog);
            Field mMessage = mAlertController.getClass().getDeclaredField("mMessageView");
            mMessage.setAccessible(true);
            TextView mMessageView = (TextView) mMessage.get(mAlertController);
            mMessageView.setTextColor(Color.BLACK);
        } catch (IllegalAccessException e) {
            e.printStackTrace();
        } catch (NoSuchFieldException e) {
            e.printStackTrace();
        }
```

#### web
* [Android-优化不同版本系统WebView版本兼容性问题](http://hjhrq1991.info/2016/08/27/TbsBridgeWebView/)
* AndroidWebView与JS交互
https://yifeng.studio/2016/12/01/android-webview-java-js-interaction/
https://75team.com/post/android-webview-and-js.html
[主流浏览器内核介绍（前端开发值得了解的浏览器内核历史）](http://web.jobbole.com/84826/)

#### volley
* 封装，参考文章
[修改volley默认超时时间以及重连次数](https://blog.csdn.net/lonewolf521125/article/details/45477187)
[网络延迟时，Volley多次request的问题解决](https://blog.csdn.net/lonewolf521125/article/details/46724373)
* Volley类库适配HTTPS
> https://www.jianshu.com/p/efbecdd9530e
> https://blog.csdn.net/lintax/article/details/69761913
> https://www.jianshu.com/p/0e1b683e6108

#### 打包发布
* [5分钟发布 Android Library 项目到 JCenter](https://github.com/panpf/android-library-publish-to-jcenter)
* [Publish an Android library on jCenter](https://medium.com/@eliaslecomte/publish-an-android-library-on-jcenter-a37770dc9570)
* [How to Publish Your Android Studio Library to JCenter](https://medium.com/@daniellevass/how-to-publish-your-android-studio-library-to-jcenter-5384172c4739)

### android-support-business
* 采用分支管理
* android-support-payment
* android-support-push
* android-support-share
* android-support-maps
* android-support-analytis

### AndroidTools需求
* [专访黑域](https://sspai.com/post/37950)

### android-practice 增加内容
* 底部导航条
```
现在大部分App底部都有一个菜单，实现这个功能也有好多办法：

TabHost+Fragment
RadioGroup+Fragment
FragmentTabHost+Fragment
5.0以后有个新控件，BottomNavigator
这篇主要介绍下FragmentTabHost配合Fragment使用

作者：Greathfs
链接：http://www.jianshu.com/p/4d4a83945193
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
```

### android 属性动画
```
// 规则页面实现优化
如果你的dialog是像上图一样上部透明，下部规整的样式，你可以考虑用layer-list和inset来实现：

<inset xmlns:android="http://schemas.android.com/apk/res/android"
    android:insetBottom="16dp"
    android:insetLeft="26dp"
    android:insetRight="26dp"
    android:insetTop="16dp"
    >

    <layer-list>
        <item>
            <color android:color="#00E4007F" />  // 透明区域
        </item>

        <item android:top="80dp">
            <shape android:shape="rectangle">
                <corners android:radius="10dp" />
                <solid android:color="#d19a70" />
            </shape>
        </item>
    </layer-list>
</inset>

作者：天之界线2010
链接：http://www.jianshu.com/p/526fcf3e8db3
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
```
```

# 使用
* Eclipse
``` xmlns:app="http://schemas.android.com/apk/res/com.yxkj.mgame"```
* AndroidStudio
```xmlns:app="http://schemas.android.com/apk/res-auto"```


<?xml version="1.0" encoding="utf-8"?>
<selector xmlns:android="http://schemas.android.com/apk/res/android" >

    <!-- 按下状态：(01) true表示按下，例如，Button被按下； (02) false表示非按下。 -->
    <item android:state_pressed="true/false" android:drawable="@drawable/exam01" />

    <!-- 聚焦状态：(01) true表示获取焦点； (02) false表示非获取焦点。 -->
    <item android:state_focused="true/false" android:drawable="@drawable/exam01" />

    <!-- 选中状态：(01) true表示选中，例如，Tab被选中； (02) false表示非选中。 -->
    <item android:state_selected="true/false" android:drawable="@drawable/exam01" />

    <!-- 可勾选状态：(01) true表示可勾选； (02) false表示不可勾选。 -->
    <item android:state_checkable="true/false" android:drawable="@drawable/exam01" />

    <!-- 选中状态：(01) true表示选中，例如，checkbox被选中； (02) false表示非选中。 -->
    <item android:state_checked="true/false" android:drawable="@drawable/exam01" />

    <!-- 使能状态：(01) true表示可用； (02) false表示不可用。 -->
    <item android:state_enabled="true/false" android:drawable="@drawable/exam01" />

    <!-- 焦点状态：(01) true表示获取焦点； (02) false表示可获取焦点。 -->
    <item android:state_window_focused="true/false" android:drawable="@drawable/exam01" />

</selector>


<?xml version="1.0" encoding="utf-8"?>
<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape=["rectangle" | "oval" | "line" | "ring"] >   --- 默认为rectangle
    android:innerRadius="dimension"  -- ring专用，内圆环的半径大小。设置innerRadius时，会忽略innerRadiusRatio
    android:innerRadiusRatio="float" -- ring专用，内圆环的半径比例。例如，比例为10表示"内圆环的半径大小=圆环宽度/10"
    android:thickness="dimension"    -- ring专用，内圆环的厚度大小。设置thickness时，会忽略thicknessRatio
    android:thicknessRatio="float"   -- ring专用，内圆环的厚度比例。例如，比例为10表示"内圆环的厚度大小=圆环宽度/10"
    android:useLevel="true|false"  -- true表示将该形状当作LevelListDrawable
    <size    -- 大小
        android:width="dimension"
        android:height="dimension" />
    <gradient  -- 渐变
        android:type=["linear" | "radial" | "sweep"] -- 渐变类型：线性，径向，扫描
        android:angle="float"   
        android:startColor="color"
        android:centerColor="color"  -- 中心点颜色
        android:endColor="color"
        android:centerX="float|fraction"  -- 中心点X坐标
        android:centerY="float|fraction"  -- 中心点Y坐标
        android:gradientRadius="float|fraction" -- 径向渐变的半径
        android:useLevel=["true" | "false"] />
    <corners  -- shape=“rectangle”时使用， 
        android:radius="dimension"  -- 四个角的半径
        android:topLeftRadius="dimension"
        android:topRightRadius="dimension"
        android:bottomLeftRadius="dimension"
        android:bottomRightRadius="dimension" />
    <padding  -- 内容与边框的距离
        android:left="dimension"
        android:top="dimension"
        android:right="dimension"
        android:bottom="dimension" />
    <solid    -- 填充颜色
        android:color="color" />
    <stroke    -- 指定边框
        android:width="dimension"
        android:color="color"
        android:dashWidth="dimension"    -- 虚线宽度
        android:dashGap="dimension" />    -- 虚线间隔宽度
</shape>

*  InputLayout自动获取焦点弹出软键盘
* step1 设置android:focusable="true" 和 android:focusableInTouchMode="true"
* step2 activity 设置 android:windowSoftInputMode="stateVisible|adjustResize"
* [Android InputMethodManager输入法简介](http://www.cnblogs.com/weixing/p/3300908.html)
```

### Kotlin学习博客系列
* [Kotlin-01.入门介绍和基础语法(Basic Syntax)](http://lioil.win/2017/06/11/Kotlin-Introduction.html)

### 项目管理博客系列

#### 版本库管理
* 结合SVN和Git

### android推送博客系列
* 友盟，魅族，极光，信鸽，小米

#### 历史
* 原生推送
* C2DM->GCM->FCM
```
Firebase Cloud Messaging
FCM是谷歌推出的最新的Android系统级别的消息推送服务（用来替换GCM）。
GCM(Google Cloud Message for Android)是Google发布的Android服务器推送（push）技术。
之前的C2DM(Android Cloud to Device Messaging)已与2012年6月26日被正式弃用。

作者：hongjay
链接：https://www.jianshu.com/p/6cf4dd76e508
來源：简书
简书著作权归作者所有，任何形式的转载都请联系作者获得授权并注明出处。
```

* 1.[原理](http://36kr.com/p/5073628.html)
* 2.[最佳选择]()
* [友盟推送集成文档](https://developer.umeng.com/docs/66632/detail/66744)
* [信鸽推送集成文档](http://docs.developer.qq.com/xg/)

* [极光推送集成文档](http://docs.jiguang.cn/jpush/client/Android/android_guide/#fcm)
```
特性:集成FCM通道，适合国内海外市场都要推送的应用
```

* [个推集成文档](http://docs.getui.com/getui/start/getting/)
```
特性:只有一个通道
```

##### 自己开发融合推送
* 极光+小米+华为+魅族
* 小米+华为+魅族+FCM
* [MixPush](https://github.com/joyrun/MixPush)


### Gradle常见设置
```
sourceSets {
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
```
