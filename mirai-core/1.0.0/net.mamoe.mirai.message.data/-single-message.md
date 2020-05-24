[mirai-core](../index.md) / [net.mamoe.mirai.message.data](index.md) / [SingleMessage](./-single-message.md)

# SingleMessage

`interface SingleMessage : `[`Message`](-message/index.md)

单个消息元素. 与之相对的是 [MessageChain](-message-chain/index.md), 是多个 [SingleMessage](./-single-message.md) 的集合.

### Extension Properties

| [content](content.md) | [Message.contentToString](-message/content-to-string.md) 的捷径`val `[`Message`](-message/index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions

| [asMessageChain](as-message-chain.md) | 直接将 [this](as-message-chain/-this-.md) 委托为一个 [MessageChain](-message-chain/index.md)`fun `[`SingleMessage`](./-single-message.md)`.asMessageChain(): `[`MessageChain`](-message-chain/index.md) |
| [flatten](flatten.md) | 扁平化 [Message](-message/index.md)`fun `[`Message`](-message/index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](./-single-message.md)`>` |
| [isContentEmpty](is-content-empty.md) | 判断消息内容是否为空.`fun `[`Message`](-message/index.md)`.isContentEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isContentNotEmpty](is-content-not-empty.md) | `fun `[`Message`](-message/index.md)`.isContentNotEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isNotPlain](is-not-plain.md) | `fun `[`Message`](-message/index.md)`.isNotPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isPlain](is-plain.md) | `fun `[`Message`](-message/index.md)`.isPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [plus](plus.md) | `suspend operator fun `[`Message`](-message/index.md)`.plus(another: Flow<`[`Message`](-message/index.md)`>): `[`MessageChain`](-message-chain/index.md) |
| [repeat](repeat.md) | 将此消息元素按顺序重复 [count](repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](-message/index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](-message-chain/index.md) |
| [sendTo](send-to.md) | `suspend fun <C : `[`Contact`](../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](-message/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` |
| [times](times.md) | 将此消息元素按顺序重复 [count](times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](-message/index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](-message-chain/index.md) |
| [toForwardMessage](to-forward-message.md) | 转换为 [ForwardMessage](-forward-message/index.md)`fun `[`Message`](-message/index.md)`.toForwardMessage(sender: `[`User`](../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](-forward-message/index.md)<br>`fun `[`Message`](-message/index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](-forward-message/index.md) |

### Inheritors

| [CustomMessage](-custom-message/index.md) | 自定义消息`sealed class CustomMessage : `[`SingleMessage`](./-single-message.md) |
| [MessageContent](-message-content.md) | 消息内容`interface MessageContent : `[`SingleMessage`](./-single-message.md) |
| [MessageMetadata](-message-metadata/index.md) | 消息元数据, 即不含内容的元素.`interface MessageMetadata : `[`SingleMessage`](./-single-message.md) |

