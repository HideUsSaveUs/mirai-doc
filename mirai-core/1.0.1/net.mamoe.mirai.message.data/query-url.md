[mirai-core](../index.md) / [net.mamoe.mirai.message.data](index.md) / [queryUrl](./query-url.md)

# queryUrl

`suspend fun `[`Image`](-image/index.md)`.queryUrl(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)

查询原图下载链接.

当图片为从服务器接收的消息中的图片时, 可以直接获取下载链接, 本函数不会挂起协程.
其他情况下协程可能会挂起并向服务器查询下载链接, 或不挂起并拼接一个链接.

### Exceptions

`IllegalStateException` - 当无任何 [Bot](../net.mamoe.mirai/-bot/index.md) 在线时抛出 (因为无法获取相关协议)

**Return**
原图 HTTP 下载链接 (非 HTTPS)

