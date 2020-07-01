[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [Message](index.md) / [plus](./plus.md)

# plus

`open operator fun plus(another: `[`MessageChain`](../-message-chain/index.md)`): `[`MessageChain`](../-message-chain/index.md)
`open operator fun plus(another: `[`Message`](index.md)`): `[`MessageChain`](../-message-chain/index.md)
`open operator fun plus(another: `[`Iterable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)`<`[`Message`](index.md)`>): `[`MessageChain`](../-message-chain/index.md)
`@JvmName("plusIterableString") open operator fun plus(another: `[`Iterable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>): `[`MessageChain`](../-message-chain/index.md)
`open operator fun plus(another: `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`Message`](index.md)`>): `[`MessageChain`](../-message-chain/index.md)

将 [another](plus.md#net.mamoe.mirai.message.data.Message$plus(net.mamoe.mirai.message.data.MessageChain)/another) 按顺序连接到这个消息的尾部.

`open operator fun plus(another: `[`SingleMessage`](../-single-message.md)`): `[`MessageChain`](../-message-chain/index.md)

将 [another](plus.md#net.mamoe.mirai.message.data.Message$plus(net.mamoe.mirai.message.data.SingleMessage)/another) 连接到这个消息的尾部.

`open operator fun plus(another: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageChain`](../-message-chain/index.md)
`open operator fun plus(another: `[`CharSequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`): `[`MessageChain`](../-message-chain/index.md)

将 [another](plus.md#net.mamoe.mirai.message.data.Message$plus(kotlin.String)/another) 作为 [PlainText](../-plain-text/index.md) 连接到这个消息的尾部.

