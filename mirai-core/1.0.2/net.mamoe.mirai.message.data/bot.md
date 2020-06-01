[mirai-core](../index.md) / [net.mamoe.mirai.message.data](index.md) / [bot](./bot.md)

# bot

`val `[`MessageChain`](-message-chain/index.md)`.bot: `[`Bot`](../net.mamoe.mirai/-bot/index.md)

消息内部 id.

仅从服务器接收的消息 (即来自 [MessageEvent.message](../net.mamoe.mirai.message/-message-event/message.md)), 或手动添加了 [MessageSource](-message-source/index.md) 元素的 [MessageChain](-message-chain/index.md) 才可以获取. 否则将抛出异常 [NoSuchElementException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-no-such-element-exception/index.html)

**See Also**

[MessageSource.id](-message-source/id.md)

`inline val `[`QuoteReply`](-quote-reply/index.md)`.bot: `[`Bot`](../net.mamoe.mirai/-bot/index.md)

**See Also**

[MessageSource.bot](-message-source/bot.md)

