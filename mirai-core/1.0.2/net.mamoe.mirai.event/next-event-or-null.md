[mirai-core](../index.md) / [net.mamoe.mirai.event](index.md) / [nextEventOrNull](./next-event-or-null.md)

# nextEventOrNull

`suspend fun <reified E : `[`Event`](-event/index.md)`> nextEventOrNull(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, priority: EventPriority = EventPriority.MONITOR): E?`

挂起当前协程, 直到监听到事件 [E](next-event-or-null.md#E) 的广播, 返回这个事件实例.

### Parameters

`timeoutMillis` - 超时. 单位为毫秒. `-1` 为不限制.

**See Also**

[subscribe](kotlinx.coroutines.-coroutine-scope/subscribe.md)

[syncFromEvent](sync-from-event.md)

**Return**
事件实例, 在超时后返回 `null`

