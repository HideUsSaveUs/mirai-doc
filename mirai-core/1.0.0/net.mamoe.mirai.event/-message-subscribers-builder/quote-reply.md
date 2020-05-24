[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [MessageSubscribersBuilder](index.md) / [quoteReply](./quote-reply.md)

# quoteReply

`open infix fun ListeningFilter<M, Ret, R, RR>.quoteReply(toReply: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): Ret`
`open infix fun ListeningFilter<M, Ret, R, RR>.quoteReply(toReply: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): Ret`

启动监听器, 在 [Bot](../../net.mamoe.mirai/-bot/index.md) 未被禁言且消息满足条件 [this](quote-reply/-this-.md) 时引用回复原消息

`open infix fun ListeningFilter<M, Ret, R, RR>.quoteReply(replier: suspend M.(`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`) -> `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?): Ret`

启动监听器, 在 [Bot](../../net.mamoe.mirai/-bot/index.md) 未被禁言且消息满足条件 [this](quote-reply/-this-.md) 时执行 [replier](quote-reply.md#net.mamoe.mirai.event.MessageSubscribersBuilder$quoteReply(net.mamoe.mirai.event.MessageSubscribersBuilder.ListeningFilter((net.mamoe.mirai.event.MessageSubscribersBuilder.M, net.mamoe.mirai.event.MessageSubscribersBuilder.Ret, net.mamoe.mirai.event.MessageSubscribersBuilder.R, net.mamoe.mirai.event.MessageSubscribersBuilder.RR)), kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.MessageSubscribersBuilder.M, kotlin.String, kotlin.Any)))/replier) 并以其返回值回复原消息
返回值 [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) 将被忽略, [Message](../../net.mamoe.mirai.message.data/-message/index.md) 将被直接回复, 其他内容将会 [Any.toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html) 后发送

