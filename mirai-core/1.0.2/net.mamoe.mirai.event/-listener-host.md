[mirai-core](../index.md) / [net.mamoe.mirai.event](index.md) / [ListenerHost](./-listener-host.md)

# ListenerHost

`interface ListenerHost`

实现这个接口的对象可以通过 [EventHandler](-event-handler/index.md) 标注事件监听函数, 并通过 [registerEvents](register-events.md) 注册.

**See Also**

[SimpleListenerHost](-simple-listener-host/index.md)

[EventHandler](-event-handler/index.md)

### Inheritors

| Name | Summary |
|---|---|
| [SimpleListenerHost](-simple-listener-host/index.md) | 携带一个异常处理器的 [ListenerHost](./-listener-host.md).`abstract class SimpleListenerHost : `[`ListenerHost`](./-listener-host.md)`, CoroutineScope` |
