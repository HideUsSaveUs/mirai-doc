[mirai-core](../index.md) / [net.mamoe.mirai.message](index.md) / [nextMessageOrNull](./next-message-or-null.md)

# nextMessageOrNull

`suspend inline fun <reified P : `[`MessageEvent`](-message-event/index.md)`> P.nextMessageOrNull(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, priority: EventPriority = EventPriority.MONITOR, noinline filter: suspend P.(P) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = { true }): `[`MessageChain`](../net.mamoe.mirai.message.data/-message-chain/index.md)`?`

挂起当前协程, 等待下一条 [MessageEvent.sender](-message-event/sender.md) 和 [MessageEvent.subject](-message-event/subject.md) 与 [this](next-message-or-null/-this-.md) 相同且通过 [筛选](next-message-or-null.md#net.mamoe.mirai.message$nextMessageOrNull(net.mamoe.mirai.message.nextMessageOrNull.P, kotlin.Long, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.message.nextMessageOrNull.P, , kotlin.Boolean)))/filter) 的 [MessageEvent](-message-event/index.md)

若 [filter](next-message-or-null.md#net.mamoe.mirai.message$nextMessageOrNull(net.mamoe.mirai.message.nextMessageOrNull.P, kotlin.Long, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.message.nextMessageOrNull.P, , kotlin.Boolean)))/filter) 抛出了一个异常, 本函数会立即抛出这个异常.

### Parameters

`timeoutMillis` - 超时. 单位为毫秒.

`filter` - 过滤器. 返回非 null 则代表得到了需要的值. [syncFromEvent](../net.mamoe.mirai.event/sync-from-event.md) 会返回这个值

**Return**
消息链. 超时时返回 `null`

**See Also**

[syncFromEventOrNull](../net.mamoe.mirai.event/sync-from-event-or-null.md)

