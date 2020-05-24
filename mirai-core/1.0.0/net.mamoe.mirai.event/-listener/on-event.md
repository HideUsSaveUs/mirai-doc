[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [Listener](index.md) / [onEvent](./on-event.md)

# onEvent

`abstract suspend fun onEvent(event: E): `[`ListeningStatus`](../-listening-status/index.md)

这个方法将会调用 [CoroutineScope.subscribe](../kotlinx.coroutines.-coroutine-scope/subscribe.md) 时提供的参数 `noinline handler: suspend E.(E) -> ListeningStatus`.

这个函数不会抛出任何异常, 详见 [CoroutineScope.subscribe](../kotlinx.coroutines.-coroutine-scope/subscribe.md)

