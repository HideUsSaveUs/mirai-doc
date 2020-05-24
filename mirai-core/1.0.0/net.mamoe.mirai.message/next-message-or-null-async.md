[mirai-core](../index.md) / [net.mamoe.mirai.message](index.md) / [nextMessageOrNullAsync](./next-message-or-null-async.md)

# nextMessageOrNullAsync

`inline fun <reified P : `[`MessageEvent`](-message-event/index.md)`> P.nextMessageOrNullAsync(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, priority: EventPriority = EventPriority.MONITOR, noinline filter: suspend P.(P) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = { true }): Deferred<`[`MessageChain`](../net.mamoe.mirai.message.data/-message-chain/index.md)`?>`

[nextMessageOrNull](next-message-or-null.md) 的异步版本

**See Also**

[nextMessageOrNull](next-message-or-null.md)

