Android studio 导入github工程


前言：载完项目先不要急着导入，按下文操作修改一些gradle相关文件后再导入

1. 第一个文件:Project-master\build.gradle

dependencies {  
        classpath 'com.android.tools.build:gradle:0.6.+'  
}

dependencies {  
        classpath 'com.android.tools.build:gradle:1.0.0'  
}


2. 第二个文件:D:\PagerSlidingTabStrip-master\gradle\wrapper\gradle-wrapper.properties

distributionUrl=http\://services.gradle.org/distributions/gradle-1.8-all.zip

项目含一个app src目录，4个测试目录，
分别是androidTest（UI层测试）、androidTestMock（UI层测试mock数据支持）、test（业务层单元测试）、mock（业务层单元测试mock数据支持）。src目录的代码组织方式完全是按照功能来组织的，功能内部分为xactivity、xcontract、xfragment、xpresenter四个类文件(x代表业务名称)。


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