[mirai-core](../index.md) / [net.mamoe.mirai.message.data](index.md) / [recall](./recall.md)

# recall

`suspend fun `[`MessageSource`](-message-source/index.md)`.recall(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)
`suspend fun `[`MessageChain`](-message-chain/index.md)`.recall(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

撤回这条消息. 可撤回自己 2 分钟内发出的消息, 和任意时间的群成员的消息.

**注意:** 仅从服务器接收的消息 (即来自 [MessageEvent.message](../net.mamoe.mirai.message/-message-event/message.md)), 或手动添加了 [MessageSource](-message-source/index.md) 元素的 [MessageChain](-message-chain/index.md) 才可以撤回.

*提示: 若要撤回一条机器人自己发出的消息, 使用 [Contact.sendMessage](../net.mamoe.mirai.contact/-contact/send-message.md) 返回的 [MessageReceipt](../net.mamoe.mirai.message/-message-receipt/index.md) 中的 [MessageReceipt.recall](../net.mamoe.mirai.message/recall.md)*

[Bot](../net.mamoe.mirai/-bot/index.md) 撤回自己的消息不需要权限.
[Bot](../net.mamoe.mirai/-bot/index.md) 撤回群员的消息需要管理员权限.

### Exceptions

`PermissionDeniedException` - 当 [Bot](../net.mamoe.mirai/-bot/index.md) 无权限操作时

`IllegalStateException` - 当这条消息已经被撤回时 (仅同步主动操作)

**See Also**

[Bot.recall](../net.mamoe.mirai/-bot/recall.md)

