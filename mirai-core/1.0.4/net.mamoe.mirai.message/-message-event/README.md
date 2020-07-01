[mirai-core](../../index.md) / [net.mamoe.mirai.message](../index.md) / [MessageEvent](./index.md)

# MessageEvent

`abstract class MessageEvent : @PlannedRemoval("1.2.0") ContactMessage, `[`BotEvent`](../../net.mamoe.mirai.event.events/-bot-event/index.md)`, `[`MessageEventExtensions`](../-message-event-extensions/index.md)`<`[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`>`

一个 (收到的) 消息事件.

它是一个 [BotEvent](../../net.mamoe.mirai.event.events/-bot-event/index.md), 因此可以被 [监听](#)

支持的消息类型:

* [群消息事件](../-group-message-event/index.md)
* [好友消息事件](../-friend-message-event/index.md)
* [临时会话消息事件](../-temp-message-event/index.md)

**See Also**

[isContextIdenticalWith](../is-context-identical-with.md)

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | 一个 (收到的) 消息事件.`MessageEvent()` |

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | 与这个消息事件相关的 [Bot](../../net.mamoe.mirai/-bot/index.md)`abstract val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |
| [message](message.md) | 消息内容.`abstract val message: `[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md) |
| [sender](sender.md) | 发送人.`abstract val sender: `[`User`](../../net.mamoe.mirai.contact/-user/index.md) |
| [senderName](sender-name.md) | 发送人名称`abstract val senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [source](source.md) | 消息源. 来自 [message](message.md) 的第一个元素,`open val source: Incoming` |
| [subject](subject.md) | 消息事件主体.`abstract val subject: `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md) |
| [time](time.md) | 消息发送时间 (由服务器提供, 可能与本地有时差)`abstract val time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
| [buildForwardMessage](../../net.mamoe.mirai.message.data/build-forward-message.md) | 使用 DSL 构建一个 [ForwardMessage](../../net.mamoe.mirai.message.data/-forward-message/index.md).`fun `[`MessageEvent`](./index.md)`.buildForwardMessage(context: `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)` = this.subject, displayStrategy: DisplayStrategy = DisplayStrategy, block: `[`ForwardMessageBuilder`](../../net.mamoe.mirai.message.data/-forward-message-builder/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`ForwardMessage`](../../net.mamoe.mirai.message.data/-forward-message/index.md) |
| [isContextIdenticalWith](../is-context-identical-with.md) | 判断两个 [MessageEvent](./index.md) 的 [MessageEvent.sender](sender.md) 和 [MessageEvent.subject](subject.md) 是否相同`fun `[`MessageEvent`](./index.md)`.isContextIdenticalWith(another: `[`MessageEvent`](./index.md)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [nextMessage](../next-message.md) | 挂起当前协程, 等待下一条 [MessageEvent.sender](sender.md) 和 [MessageEvent.subject](subject.md) 与 [this](../next-message/-this-.md) 相同且通过 [筛选](../next-message.md#net.mamoe.mirai.message$nextMessage(net.mamoe.mirai.message.nextMessage.P, kotlin.Long, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.message.nextMessage.P, , kotlin.Boolean)))/filter) 的 [MessageEvent](./index.md)`suspend fun <P : `[`MessageEvent`](./index.md)`> P.nextMessage(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, priority: EventPriority = EventPriority.MONITOR, filter: suspend P.(P) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = { true }): `[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md) |
| [nextMessageAsync](../next-message-async.md) | `fun <P : `[`MessageEvent`](./index.md)`> P.nextMessageAsync(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, priority: EventPriority = EventPriority.MONITOR, filter: suspend P.(P) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = { true }): Deferred<`[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md)`>` |
| [nextMessageOrNull](../next-message-or-null.md) | 挂起当前协程, 等待下一条 [MessageEvent.sender](sender.md) 和 [MessageEvent.subject](subject.md) 与 [this](../next-message-or-null/-this-.md) 相同且通过 [筛选](../next-message-or-null.md#net.mamoe.mirai.message$nextMessageOrNull(net.mamoe.mirai.message.nextMessageOrNull.P, kotlin.Long, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.message.nextMessageOrNull.P, , kotlin.Boolean)))/filter) 的 [MessageEvent](./index.md)`suspend fun <P : `[`MessageEvent`](./index.md)`> P.nextMessageOrNull(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, priority: EventPriority = EventPriority.MONITOR, filter: suspend P.(P) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = { true }): `[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md)`?` |
| [nextMessageOrNullAsync](../next-message-or-null-async.md) | [nextMessageOrNull](../next-message-or-null.md) 的异步版本`fun <P : `[`MessageEvent`](./index.md)`> P.nextMessageOrNullAsync(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, priority: EventPriority = EventPriority.MONITOR, filter: suspend P.(P) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = { true }): Deferred<`[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md)`?>` |
| [selectMessages](../../net.mamoe.mirai.event/select-messages.md) | 挂起当前协程, 等待任意一个事件监听器触发后返回其返回值.`suspend fun <T : `[`MessageEvent`](./index.md)`, R> T.selectMessages(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, filterContext: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true, priority: EventPriority = EventPriority.MONITOR, selectBuilder: `[`MessageSelectBuilder`](../../net.mamoe.mirai.event/-message-select-builder.md)`<T, R>.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): R` |
| [selectMessagesUnit](../../net.mamoe.mirai.event/select-messages-unit.md) | [selectMessages](../../net.mamoe.mirai.event/select-messages.md) 的 [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) 返回值捷径 (由于 Kotlin 无法推断 [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) 类型)`suspend fun <T : `[`MessageEvent`](./index.md)`> T.selectMessagesUnit(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, filterContext: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true, priority: EventPriority = EventPriority.MONITOR, selectBuilder: `[`MessageSelectBuilderUnit`](../../net.mamoe.mirai.event/-message-select-builder-unit/index.md)`<T, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`>.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [whileSelectMessages](../../net.mamoe.mirai.event/while-select-messages.md) | 挂起当前协程, 等待任意一个事件监听器返回 `false` 后返回.`suspend fun <T : `[`MessageEvent`](./index.md)`> T.whileSelectMessages(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, filterContext: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true, priority: EventPriority = EventPriority.MONITOR, selectBuilder: `[`MessageSelectBuilder`](../../net.mamoe.mirai.event/-message-select-builder.md)`<T, `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`>.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
