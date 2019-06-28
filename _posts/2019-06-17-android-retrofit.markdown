
- 创建群聊接口
```
// 字符和文件同时提交
@Multipart
@POST("/member/addgroups")
Maybe<ObjectBean> createGroupChat(@Part MultipartBody.Part name,
                                  @Part MultipartBody.Part info,
                                  @Part MultipartBody.Part location,
                                  @Part MultipartBody.Part longitude,
                                  @Part MultipartBody.Part latitude,
                                  @Part MultipartBody.Part userId,
                                  @Part MultipartBody.Part icon);
```
- 请求结构
```
POST /member/addgroups HTTP/1.1
User-Agent: Dalvik/2.1.0 (Linux; U; Android 9; Pixel Build/PPR2.181005.003) Android/com.zswh.petclub/3.0.0
Access-Token: 
Content-Type: multipart/form-data; boundary=14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Length: 28070
Host: test.pettap.cn
Connection: Keep-Alive
Accept-Encoding: gzip

--14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Disposition: form-data; name="title"
Content-Length: 0


--14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Disposition: form-data; name="info"
Content-Length: 0


--14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Disposition: form-data; name="lbs"
Content-Length: 12

海湾形成
--14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Disposition: form-data; name="longitude"
Content-Length: 10

113.940295
--14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Disposition: form-data; name="latitude"
Content-Length: 9

22.506131
--14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Disposition: form-data; name="owner_id"
Content-Length: 2

14
--14934d74-3d7c-44aa-94c9-4ad30d4de5e8
Content-Disposition: form-data; name="banner"; filename="group_chat_.png"
Content-Type: multipart/form-data
Content-Length: 27155
...文件二进制流
--14934d74-3d7c-44aa-94c9-4ad30d4de5e8--

```