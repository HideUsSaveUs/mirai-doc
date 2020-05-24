[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [CancellableEvent](index.md) / [isCancelled](./is-cancelled.md)

# isCancelled

`abstract val isCancelled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

事件是否已被取消.

事件需实现 [CancellableEvent](index.md) 接口才可以被取消,
否则此属性固定返回 false.

