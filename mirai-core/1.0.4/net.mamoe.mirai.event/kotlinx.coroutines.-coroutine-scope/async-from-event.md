[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [kotlinx.coroutines.CoroutineScope](index.md) / [asyncFromEvent](./async-from-event.md)

# asyncFromEvent

`inline fun <reified E : `[`Event`](../-event/index.md)`, R : `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`> CoroutineScope.asyncFromEvent(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, priority: EventPriority = EventPriority.MONITOR, crossinline mapper: suspend E.(E) -> R?): Deferred<R>`

异步监听这个事件, 并尝试从这个事件中获取一个值.

若 [mapper](async-from-event.md#net.mamoe.mirai.event$asyncFromEvent(kotlinx.coroutines.CoroutineScope, kotlin.Long, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.asyncFromEvent.E, , net.mamoe.mirai.event.asyncFromEvent.R)))/mapper) 抛出的异常将会被传递给 [Deferred.await](#) 抛出.

### Parameters

`timeoutMillis` - 超时. 单位为毫秒. `-1` 为不限制

`coroutineContext` - 额外的 [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)

`mapper` - 过滤转换器. 返回非 null 则代表得到了需要的值. [syncFromEvent](../sync-from-event.md) 会返回这个值

**See Also**

[syncFromEvent](../sync-from-event.md)

[asyncFromEventOrNull](async-from-event-or-null.md)

[subscribe](subscribe.md)

[nextEvent](../next-event.md)

