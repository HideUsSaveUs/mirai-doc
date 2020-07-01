[mirai-core](../../index.md) / [net.mamoe.mirai.message](../index.md) / [MessageEventExtensions](./index.md)

# MessageEventExtensions

`interface MessageEventExtensions<out TSender : `[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, out TSubject : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> : MessageEventPlatformExtensions<TSender, TSubject>`

消息事件的扩展函数

### Functions

| Name | Summary |
|---|---|
| [isBot](is-bot.md) | `open fun `[`At`](../../net.mamoe.mirai.message.data/-at/index.md)`.isBot(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [quoteReply](quote-reply.md) | 给这个消息事件的主体发送引用回复消息 对于好友消息事件, 这个方法将会给好友 ([subject](#)) 发送消息 对于群消息事件, 这个方法将会给群 ([subject](#)) 发送消息`open suspend fun quoteReply(message: `[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md)`): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>``open suspend fun quoteReply(message: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>`<br>`open suspend fun quoteReply(plain: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>` |
| [reply](reply.md) | 给这个消息事件的主体发送消息 对于好友消息事件, 这个方法将会给好友 ([subject](#)) 发送消息 对于群消息事件, 这个方法将会给群 ([subject](#)) 发送消息`open suspend fun reply(message: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>``open suspend fun reply(plain: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>` |
| [send](send.md) | `open suspend fun `[`ExternalImage`](../../net.mamoe.mirai.utils/-external-image/index.md)`.send(): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>`<br>`open suspend fun `[`Image`](../../net.mamoe.mirai.message.data/-image/index.md)`.send(): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>`<br>`open suspend fun `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`.send(): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>`<br>`open suspend fun `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`.send(): `[`MessageReceipt`](../-message-receipt/index.md)`<TSubject>` |
| [upload](upload.md) | `open suspend fun `[`ExternalImage`](../../net.mamoe.mirai.utils/-external-image/index.md)`.upload(): `[`Image`](../../net.mamoe.mirai.message.data/-image/index.md) |
| [url](url.md) | 获取图片下载链接`open suspend fun `[`Image`](../../net.mamoe.mirai.message.data/-image/index.md)`.url(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Inheritors

| Name | Summary |
|---|---|
| [MessageEvent](../-message-event/index.md) | 一个 (收到的) 消息事件.`abstract class MessageEvent : ContactMessage, `[`BotEvent`](../../net.mamoe.mirai.event.events/-bot-event/index.md)`, `[`MessageEventExtensions`](./index.md)`<`[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`>` |
