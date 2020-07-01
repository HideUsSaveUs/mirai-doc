[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [SimpleListenerHost](index.md) / [handleException](./handle-exception.md)

# handleException

`open fun handleException(context: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)`, exception: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

处理事件处理中未捕获的异常. 在构造器中的 [coroutineContext](coroutine-context.md) 未提供 [CoroutineExceptionHandler](#) 情况下必须继承此函数.

