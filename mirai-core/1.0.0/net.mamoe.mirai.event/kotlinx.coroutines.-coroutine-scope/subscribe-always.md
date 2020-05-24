[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [kotlinx.coroutines.CoroutineScope](index.md) / [subscribeAlways](./subscribe-always.md)

# subscribeAlways

`inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribeAlways(coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, concurrency: ConcurrencyKind = CONCURRENT, priority: EventPriority = NORMAL, noinline handler: suspend E.(E) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Listener`](../-listener/index.md)`<E>`

在指定的 [CoroutineScope](#) 下订阅所有 [E](subscribe-always.md#E) 及其子类事件.
每当 [事件广播](../broadcast.md) 时, [handler](subscribe-always.md#net.mamoe.mirai.event$subscribeAlways(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribeAlways.E, , kotlin.Unit)))/handler) 都会被执行.

可在任意时候通过 [Listener.complete](#) 来主动停止监听.
[CoroutineScope](#) 被关闭后事件监听会被 [取消](#).

### Parameters

`concurrency` - 并发类型默认为 [CONCURRENT](../-listener/-concurrency-kind/-c-o-n-c-u-r-r-e-n-t.md)

`coroutineContext` - 给事件监听协程的额外的 [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)

`priority` - 处理优先级, 优先级高的先执行

**Return**
监听器实例. 此监听器已经注册到指定事件上, 在事件广播时将会调用 [handler](subscribe-always.md#net.mamoe.mirai.event$subscribeAlways(kotlinx.coroutines.CoroutineScope, kotlin.coroutines.CoroutineContext, net.mamoe.mirai.event.Listener.ConcurrencyKind, net.mamoe.mirai.event.Listener.EventPriority, kotlin.coroutines.SuspendFunction2((net.mamoe.mirai.event.subscribeAlways.E, , kotlin.Unit)))/handler)

**See Also**

[CoroutineScope.subscribe](subscribe.md)

`fun <E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribeAlways(eventClass: `[`KClass`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)`<out E>, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, concurrency: ConcurrencyKind = CONCURRENT, priority: EventPriority = NORMAL, handler: suspend E.(E) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Listener`](../-listener/index.md)`<E>`

**See Also**

[CoroutineScope.subscribe](subscribe.md)

[CoroutineScope.subscribeAlways](./subscribe-always.md)

`@JvmName("subscribeAlways1") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribeAlways(crossinline handler: (E) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 带接收者的挂起函数的函数引用的监听方式.

```
fun onMessage(event: GroupMessageEvent) {

}
scope.subscribeAlways(::onMessage)
```

`@JvmName("subscribeAlways1") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribeAlways(crossinline handler: E.(E) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 带接收者的函数的函数引用的监听方式.

```
fun GroupMessageEvent.onMessage(event: GroupMessageEvent) {

}
scope.subscribeAlways(GroupMessageEvent::onMessage)
```

`@JvmName("subscribe4") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribeAlways(crossinline handler: suspend (E) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 挂起函数的函数引用的监听方式.

```
suspend fun onMessage(event: GroupMessageEvent) {

}
scope.subscribeAlways(::onMessage)
```

`@JvmName("subscribe1") inline fun <reified E : `[`Event`](../-event/index.md)`> CoroutineScope.subscribeAlways(crossinline handler: suspend E.(E) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, priority: EventPriority = NORMAL, concurrency: ConcurrencyKind = CONCURRENT, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Listener`](../-listener/index.md)`<E>`

支持 Kotlin 带接收者的挂起函数的函数引用的监听方式.

```
suspend fun GroupMessageEvent.onMessage(event: GroupMessageEvent) {

}
scope.subscribeAlways(GroupMessageEvent::onMessage)
```

