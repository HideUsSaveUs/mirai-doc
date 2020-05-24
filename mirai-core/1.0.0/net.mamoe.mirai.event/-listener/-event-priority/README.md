[mirai-core](../../../index.md) / [net.mamoe.mirai.event](../../index.md) / [Listener](../index.md) / [EventPriority](./index.md)

# EventPriority

`enum class EventPriority`

事件优先级.

在广播时, 事件监听器的调用顺序为 (从左到右):
`[HIGHEST]` -&gt; `[HIGH]` -&gt; `[NORMAL]` -&gt; `[LOW]` -&gt; `[LOWEST]` -&gt; `[MONITOR]`

* 使用 [MONITOR](-m-o-n-i-t-o-r.md) 优先级的监听器将会被**并行**调用.
* 使用其他优先级的监听器都将会**按顺序**调用.
因此一个监听器的挂起可以阻塞事件处理过程而导致低优先级的监听器较晚处理.

当事件被 [拦截](../../-event/intercept.md) 后, 优先级较低 (靠右) 的监听器将不会被调用.

### Enum Values

| Name | Summary |
|---|---|
| [HIGHEST](-h-i-g-h-e-s-t.md) |  |
| [HIGH](-h-i-g-h.md) |  |
| [NORMAL](-n-o-r-m-a-l.md) |  |
| [LOW](-l-o-w.md) |  |
| [LOWEST](-l-o-w-e-s-t.md) |  |
| [MONITOR](-m-o-n-i-t-o-r.md) | 最低的优先级. |
