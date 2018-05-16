
* 自己解决翻墙问题

## [Google API For Android](https://developers.google.com/android/)

## Google账号登录
* [官方文档](https://developers.google.com/identity/sign-in/android/)

> GoogleSignInAccount类字段值
`zzbuz = "104834795638968226733"
zzecp = {ArrayList@4789}  size = 6
zzefb = "深圳游禧科技有限公司"
zzefc = null
zzefs = "eyJhbGciOiJSUzI1NiIsImtpZCI6IjgzOWI5MjRiYjY1OWYwNzM1OGZkZjgyODhjZTU5ZjE4OWM0MDI4ZjQifQ.eyJhenAiOiIxNTU4Mzg0OTQzMTEtYjI1cGdkZHZnM2ZvNjUyamRna2xqbTVrdHE1NDk1c3QuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJhdWQiOiIxNTU4Mzg0OTQzMTEtMW5tdmthb3A4cDJzcjNpaGs1NjE3bzhnbjViMGczdmMuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJzdWIiOiIxMDQ4MzQ3OTU2Mzg5NjgyMjY3MzMiLCJlbWFpbCI6InlvdXhpa2VqaUBnbWFpbC5jb20iLCJlbWFpbF92ZXJpZmllZCI6dHJ1ZSwiZXhwIjoxNTIwMjE5MDEyLCJpc3MiOiJodHRwczovL2FjY291bnRzLmdvb2dsZS5jb20iLCJpYXQiOjE1MjAyMTU0MTIsIm5hbWUiOiLmt7HlnLPmuLjnpqfnp5HmioDmnInpmZDlhazlj7giLCJwaWN0dXJlIjoiaHR0cHM6Ly9saDQuZ29vZ2xldXNlcmNvbnRlbnQuY29tLy0zRG51NUxkbTZKMC9BQUFBQUFBQUFBSS9BQUFBQUFBQUFBQS9BR2k0Z2Z5b0NmanpOU2FNdVJiX3N6aG9oNk9DZ1BlSDVBL3M5Ni1jL3Bob3RvLmpwZyIsImdpdmVuX25hbWUiOiLmt7HlnLPmuLjnpqfnp5HmioDmnInpmZDlhazlj7giLCJsb2NhbGUiOiJ6aC1DTiJ9.YEwoi9wflPFLzLEnhkRLXybs730wvCqEt0AHbAQ_Lir9OP5m5oMkz_i2w6XndDhVFLlevKaEttHV8KRpXz2vQ1UgS8OCYNqcHYApsWUpllUBwwCrQNHs_6dRZLckHHUgHf9h5JIldo4NK2y9SziCpfDS8EaTJzFTVuJ3-F9EnmDJJDI3"
zzegs = "youxikeji@gmail.com"
zzegt = "深圳游禧科技有限公司"
zzegu = {Uri$StringUri@4794} "https://lh4.googleusercontent.com/-3Dnu5Ldm6J0/AAAAAAAAAAI/AAAAAAAAAAA/AGi4gfyoCfjzNSaMuRb_szhoh6OCgPeH5A/s96-c/photo.jpg"
zzegv = null
zzegx = "518A614DE7591DE0929B2B2B42A03995"
zzegy = {HashSet@4796}  size = 0
versionCode = 3
zzegw = 1520219012
shadow$_klass_ = {Class@4405} "class com.google.android.gms.auth.api.signin.GoogleSignInAccount"
shadow$_monitor_ = -1987686975`

## 对接Google In-app Billing
* [官方文档](https://developer.android.com/google/play/billing/index.html)
* [对接步骤](https://developer.android.com/google/play/billing/billing_integrate.html)

* 支付补单方案
> [也说iOS的In-app Purchase与Android的In-app Billing](https://blog.csdn.net/darklinden/article/details/49506087)
```
先说订单号，和iOS神奇的transaction id与7.0添加的不靠谱的applicationUsername相比，Android有透传订单号这简直是仁慈…在发起支付前就可以对订单号做跟踪，
直到订单结束都可以匹配到唯一支付，除了需要手动发自己服务器汇报参数之外简直毫无破绽。
接着是Restore，Android没有Unconsumable Purchase，相对应的是consume操作，也就是说，只要您没consume，都可以使用Restore从google服务器要上笔已支付的订单信息！
而且透传订单号在手，何愁对不上账?!当初为了处理可重复购买我在前端起sqlite存receipt数据，为了对应帐号和支付订单各种纠结，
前端不但存一堆不可靠数据，因为需要发服务器对苹果服务器验证，服务器一环报错之后也是掉单，客服天天吵吵…
    但是Android，完全可以全靠google服务器Restore确保单笔订单不丢，支付校验完成后再consume可以重复购买，依靠透传订单号确定订单唯一…简直…完美…
```
> [Unity Android 内购 In-App Billing 实现&测试经历](https://www.jianshu.com/p/af15910535cc)

```
mPurchaseMap
"com.yxkj.sdk.demo.product2" -> "PurchaseInfo(type:inapp):{"orderId":"GPA.3360-6870-5598-47074","packageName":"com.yxkj.sdk.demo","productId":"com.yxkj.sdk.demo.product2","purchaseTime":1521716698547,"purchaseState":0,"developerPayload":"CP透传字段","purchaseToken":"ngomnbepppnomemjppikpnon.AO-J1OzcnJxgS5TLL3cbw5poPsNxEHL7lTZTmIrPwYQmB1hbL0xDsOfyvWeYDTiHW1jIElgii_0nL1rImXuz9BczbKX68CH7VTyuvBQMDX3okE5uikLVm5VBP85P_xi7URZhEK3t8_uu"}"
"com.yxkj.sdk.demo.product1" -> "PurchaseInfo(type:inapp):{"orderId":"GPA.3330-1633-8375-05789","packageName":"com.yxkj.sdk.demo","productId":"com.yxkj.sdk.demo.product1","purchaseTime":1521799444891,"purchaseState":0,"developerPayload":"CP透传字段","purchaseToken":"efhmnpbbebcdmbbllhbcjpop.AO-J1OyVbyV8KqxlCTp1JlBFgzpv8FsJveEs3loEEtBrXEP1F8pBpo-_IU7Ds--5g9p7ioYEtjFtnDcxJcqOlt3z1ETEbqD_OuC9oG1Criyg3PrxE-I8bbYYrpdzt-QWcht7ABDdCM2O"}"

mSkuMap
"com.yxkj.sdk.demo.product2" -> "SkuDetails:{"productId":"com.yxkj.sdk.demo.product2","type":"inapp","price":"HK$95.90","price_amount_micros":95900000,"price_currency_code":"HKD","title":"双刀 (7477SDKDemo)","description":"这是一把双刀"}"
"com.yxkj.sdk.demo.product1" -> "SkuDetails:{"productId":"com.yxkj.sdk.demo.product1","type":"inapp","price":"HK$8.00","price_amount_micros":8000000,"price_currency_code":"HKD","title":"血瓶 (7477SDKDemo)","description":"恢复生命力"}"

inapp_data_signature=eS3/C1Rt9loJKZYLjRLY3/fGGDs5hyR1xsxncr3DqApS00S/KenTo6Z6oEG1PEu16gCPu3bJGTT71O9+EmX59VFBN15jwHeIl0E/Q60M6478OmM1h3NGDb+4Lg6wD1iyEs4QddaP7HVn/J88NyCCOg+TJg5agFVlKJYuWs8+RXFer3DPwW0XA7YcSgmTwCqcVgpg9p4wbUGZgYX1cwvR40fxOItbJy0iMKHzNWK0/xgPOZlfaCFj+LTDtLbkHikyZYKzakwRnWeRwDCmplNi1dshsSkXWnJRMa4wXcQTEgAOF1GsY3R6Fs0J8A5+r22jE0z/PTqtmemnFKkAXsRhFg==
inapp_purchase_data={"orderId":"GPA.3372-6726-2990-72178","packageName":"com.yxkj.sdk.demo","productId":"com.yxkj.sdk.demo.product1","purchaseTime":1521798569586,"purchaseState":0,"developerPayload":"CP透传字段","purchaseToken":"obmfcfjpepfpknohnfajifmc.AO-J1Oz-2GSrVGzHsqDcZ7kMOOTx0PErn3W_hbCQ1XYC9wGznsTayCWZGF5HDavAbqgL22204UecQLMdGWURz5tEv9COCWNb1VBnh4mGiWOy9L4ar5eCyk2C6uds6TSrJTf4keH-zBPp"}
```