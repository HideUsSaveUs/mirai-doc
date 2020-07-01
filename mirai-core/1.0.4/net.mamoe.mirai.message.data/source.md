[mirai-core](../index.md) / [net.mamoe.mirai.message.data](index.md) / [source](./source.md)

# source

`val `[`MessageChain`](-message-chain/index.md)`.source: `[`MessageSource`](-message-source/index.md)

获取这条消息的 [消息源](-message-source/index.md).

仅从服务器接收的消息 (即来自 [MessageEvent.message](../net.mamoe.mirai.message/-message-event/message.md)), 或手动添加了 [MessageSource](-message-source/index.md) 元素的 [MessageChain](-message-chain/index.md) 才可以获取消息源, 否则将抛出异常 [NoSuchElementException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-no-such-element-exception/index.html)

