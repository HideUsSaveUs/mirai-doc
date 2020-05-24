[mirai-core](../index.md) / [net.mamoe.mirai.message](index.md) / [nextMessageAsync](./next-message-async.md)

# nextMessageAsync

`inline fun <reified P : `[`MessageEvent`](-message-event/index.md)`> P.nextMessageAsync(timeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = -1, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext, priority: EventPriority = EventPriority.MONITOR, noinline filter: suspend P.(P) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = { true }): Deferred<`[`MessageChain`](../net.mamoe.mirai.message.data/-message-chain/index.md)`>`

**See Also**

[nextMessage](next-message.md)

