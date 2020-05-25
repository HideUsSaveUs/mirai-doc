[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [Event](./index.md)

# Event

`interface Event`

可被监听的类, 可以是任何 class 或 object.

若监听这个类, 监听器将会接收所有事件的广播.

所有 [Event](./index.md) 都应继承 [AbstractEvent](../-abstract-event/index.md) 而不要直接实现 [Event](./index.md). 否则将无法广播也无法监听.

### 广播

广播事件的唯一方式为 [broadcast](../broadcast.md).

**See Also**

[subscribeAlways](../kotlinx.coroutines.-coroutine-scope/subscribe-always.md)

[subscribeOnce](../kotlinx.coroutines.-coroutine-scope/subscribe-once.md)

[subscribeMessages](#)

[broadcast](../broadcast.md)

[CoroutineScope.subscribe](../kotlinx.coroutines.-coroutine-scope/subscribe.md)

[CancellableEvent](../-cancellable-event/index.md)

### Properties

| Name | Summary |
|---|---|
| [isIntercepted](is-intercepted.md) | 事件是否已被拦截.`abstract val isIntercepted: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |

### Functions

| Name | Summary |
|---|---|
| [intercept](intercept.md) | 拦截这个事件`abstract fun intercept(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](./index.md)`> E.__broadcastJava(): E` |
| [broadcast](../broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](./index.md)`> E.broadcast(): E` |

### Inheritors

| Name | Summary |
|---|---|
| [AbstractEvent](../-abstract-event/index.md) | 所有实现了 [Event](./index.md) 接口的类都应该继承的父类.`abstract class AbstractEvent : `[`Event`](./index.md) |
| [BotEvent](../../net.mamoe.mirai.event.events/-bot-event/index.md) | 有关一个 [Bot](../../net.mamoe.mirai/-bot/index.md) 的事件`interface BotEvent : `[`Event`](./index.md) |
| [BroadcastControllable](../-broadcast-controllable/index.md) | 可控制是否需要广播这个事件`interface BroadcastControllable : `[`Event`](./index.md) |
| [CancellableEvent](../-cancellable-event/index.md) | 可被取消的事件`interface CancellableEvent : `[`Event`](./index.md) |
| [GroupMessageEvent](../../net.mamoe.mirai.message/-group-message-event/index.md) | 机器人收到的群消息的事件`class GroupMessageEvent : GroupMessage, `[`Event`](./index.md) |
