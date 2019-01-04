---
layout: post
title:  "Android倒计时"
date:   2019-01-03 10:00
categories: jekyll update
---

- 方式一：
```
private void delayed() {
        // 延迟3S
        new Handler().postDelayed(new Runnable() {
            @Override
            public void run() {
                startActivity(new Intent(mContext, MainActivity.class));
                finish();
            }
        }, 2000);
    }
```

- 方式二：
```
Observable.timer(2000, TimeUnit.MILLISECONDS)
                .observeOn(AndroidSchedulers.mainThread())
                .subscribe(new Consumer<Long>() {
                    @Override
                    public void accept(Long aLong) throws Exception {
                        enterHomeActivity();
                    }
                });
```

### 实践
- 闪屏和引导页


- [两步打造华丽丽的Android引导页](https://lingyunzhu.github.io/2016/07/27/%E4%B8%A4%E6%AD%A5%E6%89%93%E9%80%A0%E5%8D%8E%E4%B8%BD%E4%B8%BD%E7%9A%84Android%E5%BC%95%E5%AF%BC%E9%A1%B5%EF%BC%88%E7%94%A8%E5%88%B0RxJava%EF%BC%89/)