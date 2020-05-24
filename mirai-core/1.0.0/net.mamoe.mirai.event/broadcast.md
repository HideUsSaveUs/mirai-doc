[mirai-core](../index.md) / [net.mamoe.mirai.event](index.md) / [broadcast](./broadcast.md)

# broadcast

`suspend fun <E : `[`Event`](-event/index.md)`> E.broadcast(): E`

广播一个事件的唯一途径.

当事件被实现为 Kotlin `object` 时, 同一时刻只能有一个 [广播](./broadcast.md) 存在. 较晚执行的 [广播](./broadcast.md) 将会挂起协程并等待之前的广播任务结束.

**See Also**

[__broadcastJava](__broadcast-java.md)

