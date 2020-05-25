[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [kotlinx.coroutines.CoroutineScope](index.md) / [subscribe](./subscribe.md)

# subscribe

`inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribe(coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, concurrency: ConcurrencyKind = LOCKED, priority: EventPriority = NORMAL, noinline handler: suspend E.(E) -> `[`ListeningStatus`](../-listening-status/index.md)`): `[`Listener`](../-listener/index.md)`<E>`

在指定的 [协程作用域](#) 下创建一个事件监听器, 监听所有 [E](subscribe.md#E) 及其子类事件.

每当 [事件广播](../broadcast.md) 时, [handler](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/handler) 都会被执行.

### 创建监听

调用本函数:

```
coroutineScope.subscribe<Event> { /* 会收到来自全部 Bot 的事件和与 Bot 不相关的事件 */}
```

### 生命周期

#### 通过协程作用域管理监听器

本函数将会创建一个 [Job](#), 成为 [this](subscribe/-this-.md) 中的子任务. 可创建一个 [CoroutineScope](#) 来管理所有的监听器:

```
val scope = CoroutineScope(SupervisorJob())

scope.subscribeAlways<MemberJoinEvent> { /* ... */}
scope.subscribeAlways<MemberMuteEvent> { /* ... */}

scope.cancel() // 停止上文两个监听
```

**注意**, 这个函数返回 [Listener](../-listener/index.md), 它是一个 [CompletableJob](#). 它会成为 [CoroutineScope](#) 的一个 [子任务](#)

```
runBlocking { // this: CoroutineScope
  subscribe<Event> { /* 一些处理 */} // 返回 Listener, 即 CompletableJob
}
// runBlocking 不会完结, 直到监听时创建的 `Listener` 被停止.
// 它可能通过 Listener.cancel() 停止, 也可能自行返回 ListeningStatus.Stopped 停止.
```

#### 在监听器内部停止后续监听

当 [handler](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/handler) 返回 [ListeningStatus.STOPPED](../-listening-status/-s-t-o-p-p-e-d.md) 时停止监听.
或 [Listener.complete](#) 后结束.

### 子类监听

监听父类事件, 也会同时监听其子类. 因此监听 [Event](../-event/index.md) 即可监听所有类型的事件.

### 异常处理

事件处理时的 [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) 为调用本函数时的 [receiver](subscribe/-this-.md) 的 [CoroutineScope.coroutineContext](#).
因此:

* 当参数 [handler](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/handler) 处理抛出异常时, 将会按如下顺序寻找 [CoroutineExceptionHandler](#) 处理异常:
1. 参数 [coroutineContext](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/coroutineContext)
2. 接收者 [this](subscribe/-this-.md) 的 [CoroutineScope.coroutineContext](#)
3. [Event.broadcast](../broadcast.md) 调用者的 [coroutineContext](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/coroutineContext)
4. 若事件为 [BotEvent](../../net.mamoe.mirai.event.events/-bot-event/index.md), 则从 [BotEvent.bot](../../net.mamoe.mirai.event.events/-bot-event/bot.md) 获取到 [Bot](../../net.mamoe.mirai/-bot/index.md), 进而在 [Bot.coroutineContext](../../net.mamoe.mirai/-bot/coroutine-context.md) 中寻找
5. 若以上四个步骤均无法获取 [CoroutineExceptionHandler](#), 则使用 [MiraiLogger.Companion](#) 通过日志记录. 但这种情况理论上不应发生.
* 事件处理时抛出异常不会停止监听器.
* 建议在事件处理中 (即 [handler](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/handler) 里) 处理异常,
或在参数 [coroutineContext](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/coroutineContext) 中添加 [CoroutineExceptionHandler](#).

### Parameters

`coroutineContext` - 给事件监听协程的额外的 [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html).

`concurrency` - 并发类型. 查看 [Listener.ConcurrencyKind](../-listener/-concurrency-kind/index.md)

`priority` - 监听优先级，优先级越高越先执行

`handler` - 事件处理器. 在接收到事件时会调用这个处理器. 其返回值意义参考 [ListeningStatus](../-listening-status/index.md). 其异常处理参考上文

**Return**
监听器实例. 此监听器已经注册到指定事件上, 在事件广播时将会调用 [handler](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/handler)

**See Also**

[syncFromEvent](../sync-from-event.md)

[asyncFromEvent](async-from-event.md)

[nextEvent](../next-event.md)

[selectMessages](../select-messages.md)

[whileSelectMessages](../while-select-messages.md)

[subscribeAlways](subscribe-always.md)

[subscribeOnce](subscribe-once.md)

[subscribeMessages](#)

[subscribeGroupMessages](#)

[subscribeFriendMessages](#)

[subscribeTempMessages](#)

`fun <E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribe(eventClass: `[`KClass`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)`<out E>, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, concurrency: ConcurrencyKind = LOCKED, priority: EventPriority = NORMAL, handler: suspend E.(E) -> `[`ListeningStatus`](../-listening-status/index.md)`): `[`Listener`](../-listener/index.md)`<E>`

与 [CoroutineScope.subscribe](./subscribe.md) 的区别是接受 [eventClass](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.reflect.KClass((net.mamoe.mirai.event.subscribe.E)), kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/eventClass) 参数, 而不使用 `reified` 泛型

**See Also**

[CoroutineScope.subscribe](./subscribe.md)

**Return**
监听器实例. 此监听器已经注册到指定事件上, 在事件广播时将会调用 [handler](subscribe.md#net.mamoe.mirai.event$subscribe(kotlinx.coroutines.CoroutineScope, kotlin.reflect.KClass((net.mamoe.mirai.event.subscribe.E)), kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribe.E, , net.mamoe.mirai.event.ListeningStatus)))/handler)

`@JvmName("subscribe1") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribe(crossinline handler: (E) -> `[`ListeningStatus`](../-listening-status/index.md)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 带接收者的挂起函数的函数引用的监听方式.

```
fun onMessage(event: GroupMessageEvent): ListeningStatus {
    return ListeningStatus.LISTENING
}

scope.subscribe(::onMessage)
```

`@JvmName("subscribe2") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribe(crossinline handler: E.(E) -> `[`ListeningStatus`](../-listening-status/index.md)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 带接收者的函数的函数引用的监听方式.

```
fun GroupMessageEvent.onMessage(event: GroupMessageEvent): ListeningStatus {
    return ListeningStatus.LISTENING
}

scope.subscribe(GroupMessageEvent::onMessage)
```

`@JvmName("subscribe1") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribe(crossinline handler: suspend (E) -> `[`ListeningStatus`](../-listening-status/index.md)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 挂起函数的函数引用的监听方式.

```
suspend fun onMessage(event: GroupMessageEvent): ListeningStatus {
    return ListeningStatus.LISTENING
}

scope.subscribe(::onMessage)
```

`@JvmName("subscribe3") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribe(crossinline handler: suspend E.(E) -> `[`ListeningStatus`](../-listening-status/index.md)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 带接收者的挂起函数的函数引用的监听方式.

```
suspend fun GroupMessageEvent.onMessage(event: GroupMessageEvent): ListeningStatus {
    return ListeningStatus.LISTENING
}

scope.subscribe(GroupMessageEvent::onMessage)
```

