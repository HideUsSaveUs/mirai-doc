[mirai-core](../index.md) / [net.mamoe.mirai.event](./index.md)

## Package net.mamoe.mirai.event

### Types

| Name | Summary |
|---|---|
| [AbstractEvent](-abstract-event/index.md) | 所有实现了 [Event](-event/index.md) 接口的类都应该继承的父类.`abstract class AbstractEvent : `[`Event`](-event/index.md) |
| [BroadcastControllable](-broadcast-controllable/index.md) | 可控制是否需要广播这个事件`interface BroadcastControllable : `[`Event`](-event/index.md) |
| [CancellableEvent](-cancellable-event/index.md) | 可被取消的事件`interface CancellableEvent : `[`Event`](-event/index.md) |
| [Event](-event/index.md) | 可被监听的类, 可以是任何 class 或 object.`interface Event` |
| [EventPriority](-event-priority.md) | `typealias EventPriority = EventPriority` |
| [FriendMessageSubscribersBuilder](-friend-message-subscribers-builder.md) | `typealias FriendMessageSubscribersBuilder = `[`MessageSubscribersBuilder`](-message-subscribers-builder/index.md)`<`[`FriendMessageEvent`](../net.mamoe.mirai.message/-friend-message-event/index.md)`, `[`Listener`](-listener/index.md)`<`[`FriendMessageEvent`](../net.mamoe.mirai.message/-friend-message-event/index.md)`>, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`>` |
| [GroupMessageSubscribersBuilder](-group-message-subscribers-builder.md) | `typealias GroupMessageSubscribersBuilder = `[`MessageSubscribersBuilder`](-message-subscribers-builder/index.md)`<`[`GroupMessageEvent`](../net.mamoe.mirai.message/-group-message-event/index.md)`, `[`Listener`](-listener/index.md)`<`[`GroupMessageEvent`](../net.mamoe.mirai.message/-group-message-event/index.md)`>, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`>` |
| [Listener](-listener/index.md) | 事件监听器. 由 [CoroutineScope.subscribe](kotlinx.coroutines.-coroutine-scope/subscribe.md) 等方法返回.`interface Listener<in E : `[`Event`](-event/index.md)`> : CompletableJob` |
| [ListenerHost](-listener-host.md) | 实现这个接口的对象可以通过 [EventHandler](-event-handler/index.md) 标注事件监听函数, 并通过 [registerEvents](register-events.md) 注册.`interface ListenerHost` |
| [ListeningStatus](-listening-status/index.md) | 订阅者的状态`enum class ListeningStatus` |
| [MessageListener](-message-listener.md) | 消息事件的处理器.`typealias MessageListener<T, R> = suspend T.(`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`) -> R` |
| [MessagePacketSubscribersBuilder](-message-packet-subscribers-builder.md) | `typealias MessagePacketSubscribersBuilder = `[`MessageSubscribersBuilder`](-message-subscribers-builder/index.md)`<`[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`, `[`Listener`](-listener/index.md)`<`[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`>, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`>` |
| [MessageSelectBuilder](-message-select-builder.md) | [selectMessages](select-messages.md) 时的 DSL 构建器.`abstract class MessageSelectBuilder<M : `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`, R> : `[`MessageSelectBuilderUnit`](-message-select-builder-unit/index.md)`<M, R>` |
| [MessageSelectBuilderUnit](-message-select-builder-unit/index.md) | [selectMessagesUnit](select-messages-unit.md) 或 [selectMessages](select-messages.md) 时的 DSL 构建器.`abstract class MessageSelectBuilderUnit<M : `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`, R> : `[`MessageSubscribersBuilder`](-message-subscribers-builder/index.md)`<M, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, R, `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?>` |
| [MessageSelectionTimeoutChecker](-message-selection-timeout-checker/index.md) | `class MessageSelectionTimeoutChecker` |
| [MessageSubscribersBuilder](-message-subscribers-builder/index.md) | 消息订阅构造器`open class MessageSubscribersBuilder<M : `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`, out Ret, R : RR, RR>` |
| [SimpleListenerHost](-simple-listener-host/index.md) | 携带一个异常处理器的 [ListenerHost](-listener-host.md).`abstract class SimpleListenerHost : `[`ListenerHost`](-listener-host.md)`, CoroutineScope` |
| [TempMessageSubscribersBuilder](-temp-message-subscribers-builder.md) | `typealias TempMessageSubscribersBuilder = `[`MessageSubscribersBuilder`](-message-subscribers-builder/index.md)`<`[`TempMessageEvent`](../net.mamoe.mirai.message/-temp-message-event/index.md)`, `[`Listener`](-listener/index.md)`<`[`TempMessageEvent`](../net.mamoe.mirai.message/-temp-message-event/index.md)`>, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`>` |

### Annotations

| Name | Summary |
|---|---|
| [EventHandler](-event-handler/index.md) | 标注一个函数为事件监听器.`annotation class EventHandler` |
| [MessageDsl](-message-dsl/index.md) | DSL 标记. 将能让 IDE 阻止一些错误的方法调用.`annotation class MessageDsl` |

### Exceptions

| Name | Summary |
|---|---|
| [MessageSelectionTimeoutException](-message-selection-timeout-exception/index.md) | `class MessageSelectionTimeoutException : `[`RuntimeException`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-runtime-exception/index.html) |

### Extensions for External Classes

| Name | Summary |
|---|---|
| [kotlinx.coroutines.CoroutineScope](kotlinx.coroutines.-coroutine-scope/index.md) |  |

### Properties

| Name | Summary |
|---|---|
| [EventDisabled](-event-disabled.md) | 设置为 `true` 以关闭事件. 所有的 `subscribe` 都能正常添加到监听器列表, 但所有的广播都会直接返回.`var EventDisabled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |

### Functions

| Name | Summary |
|---|---|
| [__broadcastJava](__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](-event/index.md)`> E.broadcast(): E` |
| [nextEvent](next-event.md) | 挂起当前协程, 直到监听到事件 [E](next-event.md#E) 的广播, 返回这个事件实例.`suspend fun <E : `[`Event`](-event/index.md)`> nextEvent(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, priority: EventPriority = EventPriority.MONITOR): E` |
| [nextEventOrNull](next-event-or-null.md) | 挂起当前协程, 直到监听到事件 [E](next-event-or-null.md#E) 的广播, 返回这个事件实例.`suspend fun <E : `[`Event`](-event/index.md)`> nextEventOrNull(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, priority: EventPriority = EventPriority.MONITOR): E?` |
| [registerEvents](register-events.md) | 反射得到所有标注了 [EventHandler](-event-handler/index.md) 的函数 (Java 为方法), 并注册为事件监听器`fun <T> T.registerEvents(coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)` where T : CoroutineScope, T : `[`ListenerHost`](-listener-host.md) |
| [selectMessages](select-messages.md) | 挂起当前协程, 等待任意一个事件监听器触发后返回其返回值.`suspend fun <T : `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`, R> T.selectMessages(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, filterContext: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true, priority: EventPriority = EventPriority.MONITOR, selectBuilder: `[`MessageSelectBuilder`](-message-select-builder.md)`<T, R>.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): R` |
| [selectMessagesUnit](select-messages-unit.md) | [selectMessages](select-messages.md) 的 [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) 返回值捷径 (由于 Kotlin 无法推断 [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) 类型)`suspend fun <T : `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`> T.selectMessagesUnit(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, filterContext: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true, priority: EventPriority = EventPriority.MONITOR, selectBuilder: `[`MessageSelectBuilderUnit`](-message-select-builder-unit/index.md)`<T, `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`>.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [syncFromEvent](sync-from-event.md) | 挂起当前协程, 监听事件 [E](sync-from-event.md#E), 并尝试从这个事件中**同步**一个值, 在超时时抛出 [TimeoutCancellationException](#)`suspend fun <E : `[`Event`](-event/index.md)`, R : `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`> syncFromEvent(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, priority: EventPriority = EventPriority.MONITOR, mapper: suspend E.(E) -> R?): R` |
| [syncFromEventOrNull](sync-from-event-or-null.md) | 挂起当前协程, 监听这个事件, 并尝试从这个事件中获取一个值, 在超时时返回 `null``suspend fun <E : `[`Event`](-event/index.md)`, R : `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`> syncFromEventOrNull(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, priority: EventPriority = EventPriority.MONITOR, mapper: suspend E.(E) -> R?): R?` |
| [whileSelectMessages](while-select-messages.md) | 挂起当前协程, 等待任意一个事件监听器返回 `false` 后返回.`suspend fun <T : `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`> T.whileSelectMessages(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, filterContext: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true, priority: EventPriority = EventPriority.MONITOR, selectBuilder: `[`MessageSelectBuilder`](-message-select-builder.md)`<T, `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`>.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
