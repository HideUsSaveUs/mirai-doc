[mirai-core](../index.md) / [net.mamoe.mirai.message.data](index.md) / [getOrFail](./get-or-fail.md)

# getOrFail

`@JvmOverloads inline fun <M : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.getOrFail(key: Key<M>, crossinline lazyMessage: (key: Key<M>) -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = { key.typeName }): M`

获取第一个类型为 [key](get-or-fail.md#net.mamoe.mirai.message.data$getOrFail(net.mamoe.mirai.message.data.MessageChain, net.mamoe.mirai.message.data.Message.Key((net.mamoe.mirai.message.data.getOrFail.M)), kotlin.Function1((net.mamoe.mirai.message.data.Message.Key((net.mamoe.mirai.message.data.getOrFail.M)), kotlin.String)))/key) 的 [Message](-message/index.md) 实例

### Parameters

`key` - 由各个类型消息的伴生对象持有. 如 [PlainText.Key](-plain-text/-key/index.md)