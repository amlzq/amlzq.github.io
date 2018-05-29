---
layout: post
title:  "快速入门 jekyll"
date:   2017-07-17 15:45:30 +0800
categories: jekyll update
---
### 创建
```
~ $ gem install jekyll
~ $ jekyll new myblog
~ $ cd myblog
~/myblog $ jekyll serve
# => Now browse to http://localhost:4000
```

### 本地预览
```
~ $ jekyll serve
~ # => 一个开发服务器将会运行在 http://localhost:4000/

~ $ jekyll serve --detach
~ # => 功能和`jekyll serve`命令相同，但是会脱离终端在后台运行。
~ #    如果你想关闭服务器，可以使用`kill -9 1234`命令，"1234" 是进程号（PID）。
~ #    如果你找不到进程号，那么就用`ps aux | grep jekyll`命令来查看，然后关闭服务器。[更多](http://unixhelp.ed.ac.uk/shell/jobz5.html).

~ $ jekyll serve --watch
~ # => 和`jekyll serve`相同，但是会查看变更并且自动再生成。
```

### 写作
```
安装了 Jekyll Compose 后，Jekyll 会额外提供一些命令，便于发布管理博文。

创建草稿：$ jekyll draft

创建新博客：$ jekyll post

创建新博客：$ jekyll page

发布草稿：$ jekyll publish

撤销发布：$ jekyll unpublish
```
---

### 参考文章
* [jekyll-official][jekyll-official]
* [jekyll-official-docs][jekyll-official-docs]
* [jekyll-docs][jekyll-docs]


[jekyll-official]: https://www.jekyll.com.cn/
[jekyll-official-docs]: https://www.jekyll.com.cn/docs/home/
[jekyll-docs]: https://crispgm.com/page/48-tips-for-jekyll-you-should-know.html
