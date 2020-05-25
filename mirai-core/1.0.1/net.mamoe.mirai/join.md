[mirai-core](../index.md) / [net.mamoe.mirai](index.md) / [join](./join.md)

# join

`suspend fun `[`Bot`](-bot/index.md)`.join(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

挂起协程直到 [Bot](-bot/index.md) 协程被关闭 ([Bot.close](-bot/close.md)).
即使 [Bot](-bot/index.md) 离线, 也会等待直到协程关闭.

