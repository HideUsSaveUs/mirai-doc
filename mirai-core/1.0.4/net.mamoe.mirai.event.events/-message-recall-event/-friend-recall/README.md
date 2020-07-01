[mirai-core](../../../index.md) / [net.mamoe.mirai.event.events](../../index.md) / [MessageRecallEvent](../index.md) / [FriendRecall](./index.md)

# FriendRecall

`data class FriendRecall : `[`MessageRecallEvent`](../index.md)`, Packet`

好友消息撤回事件, 暂不支持.

### Properties

| Name | Summary |
|---|---|
| [authorId](author-id.md) | 消息原发送人`val authorId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [bot](bot.md) | `val bot: `[`Bot`](../../../net.mamoe.mirai/-bot/index.md) |
| [messageId](message-id.md) | 消息 id.`val messageId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [messageInternalId](message-internal-id.md) | 消息内部 id.`val messageInternalId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [messageTime](message-time.md) | 原发送时间`val messageTime: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [operator](operator.md) | 撤回操作人, 可能为 [Bot.id](../../../net.mamoe.mirai/-bot/id.md) 或好友的 [User.id](../../../net.mamoe.mirai.contact/-user/id.md)`val operator: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
