[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [MessageSubscribersBuilder](index.md) / [reply](./reply.md)

# reply

`open infix fun ListeningFilter<M, Ret, R, RR>.reply(toReply: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): Ret`
`open infix fun ListeningFilter<M, Ret, R, RR>.reply(message: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): Ret`

启动监听器, 在 [Bot](../../net.mamoe.mirai/-bot/index.md) 未被禁言且消息满足条件 [this](reply/-this-.md) 时回复原消息

`open infix fun ListeningFilter<M, Ret, R, RR>.reply(replier: suspend M.(`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`) -> `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?): Ret`

启动监听器, 在 [Bot](../../net.mamoe.mirai/-bot/index.md) 未被禁言且消息满足条件 [this](reply/-this-.md) 时执行 [replier](reply.md#net.mamoe.mirai.event.MessageSubscribersBuilder$reply(net.mamoe.mirai.event.MessageSubscribersBuilder.ListeningFilter((net.mamoe.mirai.event.MessageSubscribersBuilder.M, net.mamoe.mirai.event.MessageSubscribersBuilder.Ret, net.mamoe.mirai.event.MessageSubscribersBuilder.R, net.mamoe.mirai.event.MessageSubscribersBuilder.RR)), kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.MessageSubscribersBuilder.M, kotlin.String, kotlin.Any)))/replier) 并以其返回值回复.
返回值 [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) 将被忽略, [Message](../../net.mamoe.mirai.message.data/-message/index.md) 将被直接回复, 其他内容将会 [Any.toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html) 后发送.

`open infix fun `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`.reply(reply: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): Ret`
`open infix fun `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`.reply(reply: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): Ret`

当发送的消息内容为 [this](reply/-this-.md) 就回复 [reply](reply.md#net.mamoe.mirai.event.MessageSubscribersBuilder$reply(kotlin.String, kotlin.String)/reply)

`open infix fun `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`.reply(replier: suspend M.(`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`) -> `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?): Ret`

当发送的消息内容为 [this](reply/-this-.md) 就执行并回复 [replier](reply.md#net.mamoe.mirai.event.MessageSubscribersBuilder$reply(kotlin.String, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.MessageSubscribersBuilder.M, kotlin.String, kotlin.Any)))/replier) 的返回值

