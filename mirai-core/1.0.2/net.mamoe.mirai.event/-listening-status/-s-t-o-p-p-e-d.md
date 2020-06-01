[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [ListeningStatus](index.md) / [STOPPED](./-s-t-o-p-p-e-d.md)

# STOPPED

`STOPPED`

表示已停止.

* 若监听器使用 [Listener.ConcurrencyKind.LOCKED](../-listener/-concurrency-kind/-l-o-c-k-e-d.md),
在这之后监听器将会被从监听器列表中删除, 因此不再能接收到事件.
* 若使用 [Listener.ConcurrencyKind.CONCURRENT](../-listener/-concurrency-kind/-c-o-n-c-u-r-r-e-n-t.md),
在这之后无法保证立即停止监听.
