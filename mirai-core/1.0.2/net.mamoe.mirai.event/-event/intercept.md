[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [Event](index.md) / [intercept](./intercept.md)

# intercept

`@SinceMirai("1.0.0") abstract fun intercept(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

拦截这个事件

当事件被 [拦截](./intercept.md) 后, 优先级较低 (靠右) 的监听器将不会被调用.

优先级为 [Listener.EventPriority.MONITOR](../-listener/-event-priority/-m-o-n-i-t-o-r.md) 的监听器不应该调用这个函数.

**See Also**

[Listener.EventPriority](../-listener/-event-priority/index.md)

