[mirai-core](../index.md) / [net.mamoe.mirai.utils](index.md) / [upload](./upload.md)

# upload

`suspend fun `[`ExternalImage`](-external-image/index.md)`.upload(contact: `[`Contact`](../net.mamoe.mirai.contact/-contact/index.md)`): `[`Image`](../net.mamoe.mirai.message.data/-image/index.md)

上传图片并构造 [Image](../net.mamoe.mirai.message.data/-image/index.md).
这个函数可能需消耗一段时间.

### Parameters

`contact` - 图片上传对象. 由于好友图片与群图片不通用, 上传时必须提供目标联系人

**See Also**

[Contact.uploadImage](../net.mamoe.mirai.contact/-contact/upload-image.md)

