[mirai-core](../../index.md) / [net.mamoe.mirai.message](../index.md) / [MessageReceipt](./index.md)

# MessageReceipt

`open class MessageReceipt<out C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`>`

发送消息后得到的回执. 可用于撤回, 引用回复等.

### Parameters

`source` - 指代发送出去的消息

`target` - 消息发送对象

**See Also**

[quote](../quote.md)

[quoteReply](../quote-reply.md)

[recall](../recall.md)

[Group.sendMessage](../../net.mamoe.mirai.contact/-group/send-message.md)

[User.sendMessage](../../net.mamoe.mirai.contact/-user/send-message.md)

[Member.sendMessage](../../net.mamoe.mirai.contact/-member/send-message.md)

[MessageReceipt.sourceId](../source-id.md)

[MessageReceipt.sourceTime](../source-time.md)

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | 发送消息后得到的回执. 可用于撤回, 引用回复等.`MessageReceipt(source: Outgoing, target: C, botAsMember: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md)`?)` |

### Properties

| Name | Summary |
|---|---|
| [botAsMember](bot-as-member.md) | `val botAsMember: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md)`?` |
| [isToGroup](is-to-group.md) | 是否为发送给群的消息的回执`val isToGroup: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [source](source.md) | 指代发送出去的消息.`val source: Outgoing` |
| [target](target.md) | 发送目标, 为 [Group](../../net.mamoe.mirai.contact/-group/index.md) 或 [Friend](../../net.mamoe.mirai.contact/-friend/index.md) 或 [Member](../../net.mamoe.mirai.contact/-member/index.md)`val target: C` |

### Functions

| Name | Summary |
|---|---|
| [__quoteBlockingForJava__](__quote-blocking-for-java__.md) | 引用这条消息.`fun __quoteBlockingForJava__(): `[`QuoteReply`](../../net.mamoe.mirai.message.data/-quote-reply/index.md) |
| [__quoteReplyBlockingForJava__](__quote-reply-blocking-for-java__.md) | 引用这条消息并回复.`fun __quoteReplyBlockingForJava__(message: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): `[`MessageReceipt`](./index.md)`<C>`<br>`fun __quoteReplyBlockingForJava__(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageReceipt`](./index.md)`<C>` |
| [__recallBlockingForJava__](__recall-blocking-for-java__.md) | 撤回这条消息. [recall](../recall.md) 或 [recallIn](../../net.mamoe.mirai/kotlinx.coroutines.-coroutine-scope/recall-in.md) 只能被调用一次.`fun __recallBlockingForJava__(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [__recallInBlockingForJava__](__recall-in-blocking-for-java__.md) | 撤回这条消息. [recall](../recall.md) 或 [recallIn](../../net.mamoe.mirai/kotlinx.coroutines.-coroutine-scope/recall-in.md) 只能被调用一次.`fun __recallInBlockingForJava__(timeMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): Job` |

### Extension Properties

| Name | Summary |
|---|---|
| [sourceId](../source-id.md) | 获取源消息 [MessageSource.id](../../net.mamoe.mirai.message.data/-message-source/id.md)`val `[`MessageReceipt`](./index.md)`<*>.sourceId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [sourceInternalId](../source-internal-id.md) | 获取源消息 [MessageSource.internalId](../../net.mamoe.mirai.message.data/-message-source/internal-id.md)`val `[`MessageReceipt`](./index.md)`<*>.sourceInternalId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [sourceTime](../source-time.md) | 获取源消息 [MessageSource.time](../../net.mamoe.mirai.message.data/-message-source/time.md)`val `[`MessageReceipt`](./index.md)`<*>.sourceTime: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [quote](../quote.md) | 引用这条消息.`fun `[`MessageReceipt`](./index.md)`<*>.quote(): `[`QuoteReply`](../../net.mamoe.mirai.message.data/-quote-reply/index.md) |
| [quoteReply](../quote-reply.md) | 引用这条消息并回复.`suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`MessageReceipt`](./index.md)`<C>.quoteReply(message: `[`Message`](../../net.mamoe.mirai.message.data/-message/index.md)`): `[`MessageReceipt`](./index.md)`<C>`<br>`suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`MessageReceipt`](./index.md)`<C>.quoteReply(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageReceipt`](./index.md)`<C>` |
| [recall](../recall.md) | 撤回这条消息. [recall](../recall.md) 或 [recallIn](../../net.mamoe.mirai/kotlinx.coroutines.-coroutine-scope/recall-in.md) 只能被调用一次.`suspend fun `[`MessageReceipt`](./index.md)`<*>.recall(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [recallIn](../recall-in.md) | 在一段时间后撤回这条消息. [recall](../recall.md) 或 [recallIn](../../net.mamoe.mirai/kotlinx.coroutines.-coroutine-scope/recall-in.md) 只能被调用一次.`fun `[`MessageReceipt`](./index.md)`<*>.recallIn(timeMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): Job` |
