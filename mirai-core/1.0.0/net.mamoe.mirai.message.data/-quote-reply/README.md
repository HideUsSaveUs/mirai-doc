[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [QuoteReply](./index.md)

# QuoteReply

`class QuoteReply : `[`Message`](../-message/index.md)`, `[`MessageMetadata`](../-message-metadata/index.md)`, `[`ConstrainSingle`](../-constrain-single/index.md)`<`[`QuoteReply`](./index.md)`>`

引用回复.

支持引用任何一条消息发送给任何人.

#### 元数据

[QuoteReply](./index.md) 被作为 [MessageMetadata](../-message-metadata/index.md), 因为它不包含实际的消息内容, 且只能在消息中单独存在.

#### [source](source.md) 的类型:

* 在发送引用回复时, [source](source.md) 类型为 [OnlineMessageSource](../-online-message-source/index.md) 或 [OfflineMessageSource](../-offline-message-source/index.md)
* 在接收引用回复时, [source](source.md) 类型一定为 [OfflineMessageSource](../-offline-message-source/index.md)

#### 原消息内容

引用回复的原消息内容完全由 [source](source.md) 中 [MessageSource.originalMessage](../-message-source/original-message.md) 控制, 客户端不会自行寻找原消息.

#### 客户端内跳转

客户端在跳转原消息时, 会通过 [MessageSource.id](../-message-source/id.md) 等 metadata

**See Also**

[MessageSource](../-message-source/index.md)

### Types

| Name | Summary |
|---|---|
| [Key](-key/index.md) | `companion object Key : Key<`[`QuoteReply`](./index.md)`>` |

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | 引用回复.`QuoteReply(source: `[`MessageSource`](../-message-source/index.md)`)` |

### Properties

| Name | Summary |
|---|---|
| [key](key.md) | 用于判断是否为同一种元素的 [Key](../-message/-key/index.md)`val key: Key<`[`QuoteReply`](./index.md)`>` |
| [source](source.md) | `val source: `[`MessageSource`](../-message-source/index.md) |

### Functions

| Name | Summary |
|---|---|
| [equals](equals.md) | `fun equals(other: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [hashCode](hash-code.md) | `fun hashCode(): `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [toString](to-string.md) | 得到包含 mirai 消息元素代码的, 易读的字符串. 如 `At(member) + "test"` 将转为 `"[mirai:at:qqId]test"``fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Companion Object Properties

| Name | Summary |
|---|---|
| [typeName](type-name.md) | 此 [Key](../-message/-key/index.md) 指代的 [Message](../-message/index.md) 类型名. 一般为 `class.simpleName`, 如 "QuoteReply", "PlainText"`val typeName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Properties

| Name | Summary |
|---|---|
| [bot](../bot.md) | `val `[`QuoteReply`](./index.md)`.bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |
| [content](../content.md) | [Message.contentToString](../-message/content-to-string.md) 的捷径`val `[`Message`](../-message/index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [flatten](../flatten.md) | 扁平化 [Message](../-message/index.md)`fun `[`Message`](../-message/index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](../-single-message.md)`>` |
| [isContentEmpty](../is-content-empty.md) | 判断消息内容是否为空.`fun `[`Message`](../-message/index.md)`.isContentEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isContentNotEmpty](../is-content-not-empty.md) | `fun `[`Message`](../-message/index.md)`.isContentNotEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isNotPlain](../is-not-plain.md) | `fun `[`Message`](../-message/index.md)`.isNotPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isPlain](../is-plain.md) | `fun `[`Message`](../-message/index.md)`.isPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [plus](../plus.md) | `suspend operator fun `[`Message`](../-message/index.md)`.plus(another: Flow<`[`Message`](../-message/index.md)`>): `[`MessageChain`](../-message-chain/index.md) |
| [recallSource](../recall-source.md) | 撤回引用的源消息`suspend fun `[`QuoteReply`](./index.md)`.recallSource(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [recallSourceIn](../recall-source-in.md) | 在一段时间后撤回引用的源消息`fun `[`QuoteReply`](./index.md)`.recallSourceIn(millis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): Job` |
| [repeat](../repeat.md) | 将此消息元素按顺序重复 [count](../repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](../-message/index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) |
| [sendTo](../send-to.md) | `suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](../-message/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` |
| [times](../times.md) | 将此消息元素按顺序重复 [count](../times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](../-message/index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) |
| [toForwardMessage](../to-forward-message.md) | 转换为 [ForwardMessage](../-forward-message/index.md)`fun `[`Message`](../-message/index.md)`.toForwardMessage(sender: `[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md)<br>`fun `[`Message`](../-message/index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md) |
