[mirai-core](../../index.md) / [net.mamoe.mirai.message](../index.md) / [MessageEventExtensions](index.md) / [reply](./reply.md)

# reply

`open suspend fun reply(message: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>`

给这个消息事件的主体发送消息
对于好友消息事件, 这个方法将会给好友 ([subject](#)) 发送消息
对于群消息事件, 这个方法将会给群 ([subject](#)) 发送消息

`open suspend fun reply(plain: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>`