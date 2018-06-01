# _drafts文件夹说明文档
---

## 模板
```
---
layout: post
title:  "填写标题"
date:   1970-01-01 00:00 +0800
categories: jekyll update
---
### 正文
---
### 参考文章
* [文字说明][文字说明]
---
[文字说明]: 链接
```

---
## 需要理解的

### Java JDK的jre和Android Studio的jre区分和联系
* C:\Program Files\Java\jdk1.8.0_25\jre
* I:\Android\android-studio-ide-171.4443003-windows\android-studio\jre

### Android多线程下载
* https://github.com/AigeStudio/MultiThreadDownloader
* https://github.com/Jerrywen/MultiThreadDownloader

### Android定位服务
* [安卓定位及坐标转换](https://www.jianshu.com/p/ddc6141bac95)
* [原生API实现](http://blog.csdn.net/luosiye312/article/details/50562309)

### 适配HTTPS
* 原声API类库
> https://juejin.im/entry/575ab9b36be3ff0069492bc6
* Volley类库
> https://www.jianshu.com/p/efbecdd9530e
> https://blog.csdn.net/lintax/article/details/69761913
> https://www.jianshu.com/p/0e1b683e6108

### 改造volley
* 参考文章
[修改volley默认超时时间以及重连次数](https://blog.csdn.net/lonewolf521125/article/details/45477187)
[网络延迟时，Volley多次request的问题解决](https://blog.csdn.net/lonewolf521125/article/details/46724373)

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


### Android技术调研-定位服务


### 2018-05-11-Android DragLayout
* 可供拖动的布局

* LayoutInflater.from(mContext).inflate(R.layout.sdk7477_widget_floatmenu, null)
* 搞明白，这个参数的作用，草草草
* root Optional view to be the parent of the generated hierarchy.

* [可以在android实践的github项目中敲一遍](https://juejin.im/entry/58133085128fe100557e4579)


### Java 反射

## 参考文章
* [一篇文章带你学懂Java反射-ming152](https://mp.weixin.qq.com/s?__biz=MzA5MzI3NjE2MA==&mid=2650242963&idx=1&sn=708e4fa01823b7844494ecb276a3733f&chksm=88638efcbf1407eaf0b5438f824a42a1890ab6a623108990cbbc1d424594ee08e9ff973ff70f&scene=0#rd)
* []()


### androidSDK目录说明
1. add-ons：这里面保存着附加库，比如Google Maps，当然你如果安装了OphoneSDK，这里也会有一些类库在里面。
2. docs：这里面是Android SDK API参考文档，所有的API都可以在这里查到。
3. market_licensing：作为AndroidMarket版权保护组件，一般发布付费应用到电子市场可以用它来反盗版。
4. platforms：是每个平台的SDK真正的文件，里面会根据API Level划分的SDK版本， 这里就以Android 2.2来说，进入后有一个android-8的文件夹，android-8进入后是Android 2.2 SDK的主要文件，其中ant为ant编译脚本，data保存着一些系统资源，images是模拟器映像文件，skins则是Android模拟器的皮肤，templates是工程创建的默认模板，android.jar则是该版本的主要framework文件，tools目录里面包含了重要的编译工具，比如aapt、aidl、逆向调试工具dexdump和编译脚本dx。

5. platform-tools：保存着一些通用工具，比如adb、和aapt、aidl、dx等文件，这里和platforms目录中tools文件夹有些重复，主要是从android 2.3开始这些工具被划分为通用了。
6. samples：是Android SDK自带的默认示例工程，里面的apidemos强烈推荐初学者运行学习，对于SQLite数据库操作可以查看NotePad这个例子，对于游戏开发Snake、LunarLander都是不错的例子，对于Android主题开发Home则是android m5时代的主题设计原理。
7. tools：作为SDK根目录下的tools文件夹，这里包含了重要的工具，比如ddms用于启动Android调试工具，比如logcat、屏=幕截图和文件管理器，而draw9patch则是绘制android平台的可缩放png图片的工具，sqlite3可以在PC上操作SQLite数据库，而monkeyrunner则是一个不错的压力测试应用，模拟用户随机按键，mksdcard则是模拟器SD映像的创建工具，emulator是android模拟器主程序，不过从android1.5开始，需要输入合适的参数才能启动模拟器，traceview作为android平台上重要的调试工具。

8. usb_drive：顾名思义，保存着android平台google官方机型的驱动如nexus one、nexus s，同时也有一些老机型驱动的支持，比如说htc dream、htc magic和motorola的droid。
//新增或修改
9.extras 扩展插件
10.system-images模拟器映像文件,从android-14开始将模拟器映像文件整理在这里(原来放在platforms下)
11.temp临时目录
12.sources源码

### AS项目结构
项目含一个app src目录，4个测试目录，
分别是androidTest（UI层测试）、androidTestMock（UI层测试mock数据支持）、test（业务层单元测试）、mock（业务层单元测试mock数据支持）。src目录的代码组织方式完全是按照功能来组织的，功能内部分为xactivity、xcontract、xfragment、xpresenter四个类文件(x代表业务名称)。

### android-support-business
* 采用分支管理
* android-support-payment
* android-support-push
* android-support-share
* android-support-maps
* android-support-analytis

### 泡椒网游戏SDK
* [Jianbo Peng](https://github.com/pengjianbo?tab=repositories)
> 

### 融合渠道SDK的技术分析
* [huanleyouren](https://github.com/huanleyouren)
* [QuickSDKTool_Win_P34](https://github.com/huanleyouren/QuickSDKTool_Win_P34)
* Fusion Game sdk 聚合游戏sdk

### 悬浮视图
* [泡椒网游戏SDK Float View(悬浮窗)](https://github.com/pengjianbo/FloatViewFinal)


### CMDB
* [open-cmdb/cmdb](https://github.com/open-cmdb/cmdb)

### 构建模板android项目仓库
* 必要的类
```
GlobalApplication
Config
```
```
@Override
protected void onDestroy() {
    super.onDestroy();
    handler.removeCallbacksAndMessages(null);
}
```

### 解决警告方法
```
@SuppressWarnings(value = {"unused", "unchecked", "deprecation"})
```

### 热更新
dex分包方案


### Logcat
```
logcat 错误 tag
E/AndroidRuntime: FATAL EXCEPTION: main
```

### 服务端返回的数据格式
```
1. data:[]
列表数据为空有两种情况
```


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

# InputLayout自动获取焦点弹出软键盘
* step1 设置android:focusable="true" 和 android:focusableInTouchMode="true"
* step2 activity 设置 android:windowSoftInputMode="stateVisible|adjustResize"
* [Android InputMethodManager输入法简介](http://www.cnblogs.com/weixing/p/3300908.html)
```

### android 遇到问题已经解决的方案
```
# 如何在Activity/Fragment结束时处理异步回调？
* [1.0](http://iluhcm.com/2017/03/05/handle-asynchronous-callbacks-when-activity-finishes/)
* [1.1](https://easytoforget.github.io/2017/07/25/handle-callback-while-activity-or-fragment-finished/)
* [1.2](https://github.com/EasyToForget/LifefulDemo)
* [1.2](https://github.com/EasyToForget/LifefulDemo)

# Android Fragment 的使用，一些你不可不知的注意事项
* [1.0](http://yifeng.studio/2016/12/15/android-fragment-attentions/)

# 如何在回调时判断Activity，Fragment，ImageView等等是否已经被关闭
* [1.0](http://note.tyz.ren/blog/post/zerozhiqin/%E5%A6%82%E4%BD%95%E5%9C%A8%E5%9B%9E%E8%B0%83%E6%97%B6%E5%88%A4%E6%96%ADActivity%EF%BC%8CFragment%EF%BC%8CImageView%E7%AD%89%E7%AD%89%E6%98%AF%E5%90%A6%E5%B7%B2%E7%BB%8F%E8%A2%AB%E5%85%B3%E9%97%AD)
```