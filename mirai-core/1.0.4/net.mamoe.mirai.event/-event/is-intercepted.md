[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [Event](index.md) / [isIntercepted](./is-intercepted.md)

# isIntercepted

`abstract val isIntercepted: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

事件是否已被拦截.

所有事件都可以被拦截, 拦截后低优先级的监听器将不会处理到这个事件.

**See Also**

[intercept](intercept.md)

