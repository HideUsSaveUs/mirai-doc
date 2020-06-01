[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [CancellableEvent](index.md) / [cancel](./cancel.md)

# cancel

`abstract fun cancel(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

取消这个事件.
事件需实现 [CancellableEvent](index.md) 接口才可以被取消

### Exceptions

`IllegalStateException` - 当事件未实现接口 [CancellableEvent](index.md) 时抛出