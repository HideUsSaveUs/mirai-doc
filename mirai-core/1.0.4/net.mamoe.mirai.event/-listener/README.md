[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [Listener](./index.md)

# Listener

`interface Listener<in E : `[`Event`](../-event/index.md)`> : CompletableJob`

事件监听器.
由 [CoroutineScope.subscribe](../kotlinx.coroutines.-coroutine-scope/subscribe.md) 等方法返回.

取消监听: [complete](#)

### Types

| Name | Summary |
|---|---|
| [ConcurrencyKind](-concurrency-kind/index.md) | `enum class ConcurrencyKind` |
| [EventPriority](-event-priority/index.md) | 事件优先级.`enum class EventPriority` |

### Properties

| Name | Summary |
|---|---|
| [concurrencyKind](concurrency-kind.md) | 并发类型`abstract val concurrencyKind: ConcurrencyKind` |
| [priority](priority.md) | 事件优先级`open val priority: EventPriority` |

### Functions

| Name | Summary |
|---|---|
| [onEvent](on-event.md) | 这个方法将会调用 [CoroutineScope.subscribe](../kotlinx.coroutines.-coroutine-scope/subscribe.md) 时提供的参数 `noinline handler: suspend E.(E) -> ListeningStatus`.`abstract suspend fun onEvent(event: E): `[`ListeningStatus`](../-listening-status/index.md) |
