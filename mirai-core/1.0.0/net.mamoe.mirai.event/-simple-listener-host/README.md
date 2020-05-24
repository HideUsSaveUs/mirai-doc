[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [SimpleListenerHost](./index.md)

# SimpleListenerHost

`abstract class SimpleListenerHost : `[`ListenerHost`](../-listener-host.md)`, CoroutineScope`

携带一个异常处理器的 [ListenerHost](../-listener-host.md).

**See Also**

[ListenerHost](../-listener-host.md)

[EventHandler](../-event-handler/index.md)

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | 携带一个异常处理器的 [ListenerHost](../-listener-host.md).`SimpleListenerHost(coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext)` |

### Properties

| Name | Summary |
|---|---|
| [coroutineContext](coroutine-context.md) | `val coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) |

### Functions

| Name | Summary |
|---|---|
| [cancelAll](cancel-all.md) | 停止所有事件监听`fun cancelAll(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [handleException](handle-exception.md) | 处理事件处理中未捕获的异常. 在构造器中的 [coroutineContext](coroutine-context.md) 未提供 [CoroutineExceptionHandler](#) 情况下必须继承此函数.`open fun handleException(context: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)`, exception: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
