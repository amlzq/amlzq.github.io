---
layout: post
title:  "Android WebView处理HTTPS"
date:   2018-09-06 10:43
categories: jekyll update
---

### 2步处理
* webview设置
```
    // 处理https，android 5.0以上默认不支持Mixed Content
    if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.LOLLIPOP) {
        webSettings.setMixedContentMode(WebSettings.MIXED_CONTENT_COMPATIBILITY_MODE);
        webSettings.setMixedContentMode(WebSettings.MIXED_CONTENT_ALWAYS_ALLOW); //设置允许加载混合内容
    }
```
* 忽略SSL证书错误
```
	private WebViewClient mWebViewClient = new WebViewClient() {

        @Override
        public void onReceivedSslError(WebView view, final SslErrorHandler handler, SslError error) {
            // super.onReceivedSslError(view, handler, error);
            handler.proceed(); // 忽略SSL证书错误(Ignore SSL certificate errors)，以下方法会被googlePlay拒审,实施方式不安全
        }

    };
```

### 按GooglePlay审核要求处理
* 忽略SSL证书错误
```
	private WebViewClient mWebViewClient = new WebViewClient() {

        @Override
        public void onReceivedSslError(WebView view, final SslErrorHandler handler, SslError error) {
            // super.onReceivedSslError(view, handler, error);
            final AlertDialog.Builder builder = new AlertDialog.Builder(mContext);
            builder.setMessage("SSL证书无效");
            builder.setPositiveButton(android.R.string.ok, new DialogInterface.OnClickListener() {
                @Override
                public void onClick(DialogInterface dialog, int which) {
                    handler.proceed(); // 忽略SSL证书错误(Ignore SSL certificate errors)，以下方法会被googlePlay拒审,实施方式不安全
                }
            });
            builder.setNegativeButton(android.R.string.cancel, new DialogInterface.OnClickListener() {
                @Override
                public void onClick(DialogInterface dialog, int which) {
                    handler.cancel(); // Android默认的处理方式
                }
            });
            final AlertDialog dialog = builder.create();
            dialog.show();
        }

    };
```

### 参考文章
* [android 用webview加载网页(https和http)](https://blog.csdn.net/qq_30740239/article/details/54141106)
* [【Android】WebView加载https页面不能正常显示资源问题)](https://blog.csdn.net/Crazy_zihao/article/details/51557425)