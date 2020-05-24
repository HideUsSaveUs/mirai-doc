[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [Voice](./index.md)

# Voice

`class Voice : `[`PttMessage`](../-ptt-message/index.md)

语音消息, 目前只支持接收和转发

### Types
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Key](-key/index.md) | `companion object Key : Key<`[`Voice`](./index.md)`>` |

### Constructors
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [&lt;init&gt;](-init-.md) | 语音消息, 目前只支持接收和转发`Voice(fileName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, md5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, _url: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` |

### Properties
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [fileName](file-name.md) | `val fileName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [md5](md5.md) | `val md5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [url](url.md) | `val url: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Functions
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [contentToString](content-to-string.md) | 转为最接近官方格式的字符串. 如 `At(member) + "test"` 将转为 `"@群名片 test"`.`fun contentToString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toString](to-string.md) | 得到包含 mirai 消息元素代码的, 易读的字符串. 如 `At(member) + "test"` 将转为 `"[mirai:at:qqId]test"``fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Companion Object Properties
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [typeName](type-name.md) | 此 [Key](../-message/-key/index.md) 指代的 [Message](../-message/index.md) 类型名. 一般为 `class.simpleName`, 如 "QuoteReply", "PlainText"`val typeName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Properties
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [content](../content.md) | [Message.contentToString](../-message/content-to-string.md) 的捷径`val `[`Message`](../-message/index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [flatten](../flatten.md) | 扁平化 [Message](../-message/index.md)`fun `[`Message`](../-message/index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](../-single-message.md)`>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isContentEmpty](../is-content-empty.md) | 判断消息内容是否为空.`fun `[`Message`](../-message/index.md)`.isContentEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isContentNotEmpty](../is-content-not-empty.md) | `fun `[`Message`](../-message/index.md)`.isContentNotEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isNotPlain](../is-not-plain.md) | `fun `[`Message`](../-message/index.md)`.isNotPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isPlain](../is-plain.md) | `fun `[`Message`](../-message/index.md)`.isPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [plus](../plus.md) | `suspend operator fun `[`Message`](../-message/index.md)`.plus(another: Flow<`[`Message`](../-message/index.md)`>): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [repeat](../repeat.md) | 将此消息元素按顺序重复 [count](../repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](../-message/index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sendTo](../send-to.md) | `suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](../-message/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [times](../times.md) | 将此消息元素按顺序重复 [count](../times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](../-message/index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toForwardMessage](../to-forward-message.md) | 转换为 [ForwardMessage](../-forward-message/index.md)`fun `[`Message`](../-message/index.md)`.toForwardMessage(sender: `[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md)<br>`fun `[`Message`](../-message/index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md) |

