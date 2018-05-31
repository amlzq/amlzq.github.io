---
layout: post
title:  "AndroidV4支持库介绍"
date:   2017-09-22 22:00 +0800
categories: jekyll update
---
### 
```
v4 支持库
v4 compat 库
v4 core-utils 库
v4 core-ui 库
v4 media-compat 库
v4 fragment 库
```

v4 支持库
这些库旨在与 Android 2.3（API 级别 9）及更高版本搭配使用。与其他支持库相比，它们包含的 API 集合最大，包括对应用组件、用户界面功能、辅助功能、数据处理、网络连接以及编程实用工具的支持。

如需了解有关 v4 支持库所提供类和方法的完整详细信息，请参阅 API 参考中的 android.support.v4 软件包。

注：在支持库修订版 24.2.0 之前，存在一个 v4 支持库。为了提高效率，此库拆分成多个模块。出于向后兼容的考虑，如果您在 Gradle 脚本中列出了 support-v4，您的 APK 将包含所有的 v4 模块。不过，要减少 APK 大小，我们建议仅列出应用需要的特定模块。

v4 compat 库
为众多框架 API 提供兼容性包装器，例如 Context.obtainDrawable() 和 View.performAccessibilityAction()。

此库的 Gradle 构建脚本依赖关系标识符如下所示：

com.android.support:support-compat:24.2.0
v4 core-utils 库
提供大量实用程序类，例如 AsyncTaskLoader 和 PermissionChecker。

此库的 Gradle 构建脚本依赖关系标识符如下所示：

com.android.support:support-core-utils:24.2.0
v4 core-ui 库
实现各种 UI 相关组件，例如 ViewPager、NestedScrollView 和 ExploreByTouchHelper。

此库的 Gradle 构建脚本依赖关系标识符如下所示：

com.android.support:support-core-ui:24.2.0
v4 media-compat 库
向后移植部分媒体框架，包括 MediaBrowser 和 MediaSession。

此库的 Gradle 构建脚本依赖关系标识符如下所示：

com.android.support:support-media-compat:24.2.0
v4 fragment 库
添加对使用片段封装用户界面和功能的支持，从而使应用能够提供可以在大屏幕设备与小屏幕设备之间进行调节的布局。此模块依赖于 compat、core-utils、core-ui 和 media-compat。

此库的 Gradle 构建脚本依赖关系标识符如下所示：

com.android.support:support-fragment:24.2.0`
---
### 参考文章
* [android.support.v4](https://developer.android.com/topic/libraries/support-library/features.html#v4-compat)
---
[文字说明]: 链接