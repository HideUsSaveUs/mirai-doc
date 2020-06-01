[mirai-core](../index.md) / [net.mamoe.mirai.event](index.md) / [registerEvents](./register-events.md)

# registerEvents

`@JvmOverloads fun <T> T.registerEvents(coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)` where T : CoroutineScope, T : `[`ListenerHost`](-listener-host.md)

反射得到所有标注了 [EventHandler](-event-handler/index.md) 的函数 (Java 为方法), 并注册为事件监听器

Java 使用: `Events.registerEvents(listenerHost)`

**See Also**

[EventHandler](-event-handler/index.md)

