[mirai-core](../index.md) / [net.mamoe.mirai.message.data](index.md) / [MessageContent](./-message-content.md)

# MessageContent

`interface MessageContent : `[`SingleMessage`](-single-message.md)

消息内容

**See Also**

[PlainText](-plain-text/index.md)

[At](-at/index.md)

[AtAll](-at-all/index.md)

[HummerMessage](-hummer-message/index.md)

[Image](-image/index.md)

[RichMessage](-rich-message/index.md)

[ServiceMessage](-service-message/index.md)

[Face](-face/index.md)

[ForwardMessage](-forward-message/index.md)

[Voice](-voice/index.md)

### Extension Properties

| [content](content.md) | [Message.contentToString](-message/content-to-string.md) 的捷径`val `[`Message`](-message/index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions

| [flatten](flatten.md) | 扁平化 [Message](-message/index.md)`fun `[`Message`](-message/index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](-single-message.md)`>` |
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

| [At](-at/index.md) | At 一个群成员. 只能发送给一个群.`data class At : `[`MessageContent`](./-message-content.md) |
| [AtAll](-at-all/index.md) | "@全体成员".`object AtAll : Key<`[`AtAll`](-at-all/index.md)`>, `[`MessageContent`](./-message-content.md) |
| [Face](-face/index.md) | QQ 自带表情`data class Face : `[`MessageContent`](./-message-content.md) |
| [FlashImage](-flash-image/index.md) | 闪照`sealed class FlashImage : `[`MessageContent`](./-message-content.md)`, `[`HummerMessage`](-hummer-message/index.md) |
| [ForwardMessage](-forward-message/index.md) | 合并转发消息`class ForwardMessage : `[`MessageContent`](./-message-content.md) |
| [HummerMessage](-hummer-message/index.md) | 一些特殊的消息`sealed class HummerMessage : `[`MessageContent`](./-message-content.md) |
| [Image](-image/index.md) | 自定义表情 (收藏的表情) 和普通图片.`interface Image : `[`Message`](-message/index.md)`, `[`MessageContent`](./-message-content.md) |
| [PlainText](-plain-text/index.md) | 纯文本. 可含 emoji 表情如 😊.`data class PlainText : `[`MessageContent`](./-message-content.md) |
| [PttMessage](-ptt-message/index.md) | 需要通过上传到服务器的消息，如语音、文件`abstract class PttMessage : `[`MessageContent`](./-message-content.md) |
| [RichMessage](-rich-message/index.md) | XML, JSON 消息等富文本消息`interface RichMessage : `[`MessageContent`](./-message-content.md) |

