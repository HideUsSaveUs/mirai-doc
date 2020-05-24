[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [Message](./index.md)

# Message

`interface Message`

可发送的或从服务器接收的消息.

[消息](./index.md) 分为

* [SingleMessage](../-single-message.md):
* [MessageMetadata](../-message-metadata/index.md) 消息元数据, 即消息的属性. 包括: [消息来源](../-message-source/index.md), [引用回复](../-quote-reply/index.md).
* [MessageContent](../-message-content.md) 含内容的消息, 包括: [纯文本](../-plain-text/index.md), [@群员](../-at/index.md), [@全体成员](../-at-all/index.md) 等.
* [MessageChain](../-message-chain/index.md): 不可变消息链, 链表形式链接的多个 [SingleMessage](../-single-message.md) 实例.

#### 在 Kotlin 使用 [Message](./index.md):

这与使用 [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) 的使用非常类似.

* 比较 [SingleMessage](../-single-message.md) 与 [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):
`if(message.content == "你好") friend.sendMessage(event)`

* 连接 [Message](./index.md) 与 [Message](./index.md), [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), (使用操作符 [Message.plus](plus.md)):

```
val text = PlainText("Hello ") + PlainText("world") + "!"
friend.sendMessage(text)
```

但注意: 不能 `String + Message`. 只能 `Message + String`

#### 实现规范

除 [MessageChain](../-message-chain/index.md) 外, 所有 [Message](./index.md) 的实现类都有伴生对象实现 [Key](-key/index.md) 接口.

#### 发送消息

* 通过 [Contact](../../net.mamoe.mirai.contact/-contact/index.md) 中的成员函数: [Contact.sendMessage](../../net.mamoe.mirai.contact/-contact/send-message.md)
* 通过 [Message](./index.md) 的扩展函数: [Message.sendTo](../send-to.md)
* 在 [MessageEvent](../../net.mamoe.mirai.message/-message-event/index.md) 中使用 [MessageEvent.reply](#) 等捷径

**See Also**

[PlainText](../-plain-text/index.md)

[Image](../-image/index.md)

[Face](../-face/index.md)

[At](../-at/index.md)

[AtAll](../-at-all/index.md)

[QuoteReply](../-quote-reply/index.md)

[RichMessage](../-rich-message/index.md)

[HummerMessage](../-hummer-message/index.md)

[CustomMessage](../-custom-message/index.md)

[MessageChain](../-message-chain/index.md)

[buildMessageChain](../build-message-chain.md)

[Contact.sendMessage](../../net.mamoe.mirai.contact/-contact/send-message.md)

### Types
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Key](-key/index.md) | 类型 Key. 由伴生对象实现, 表示一个 [Message](./index.md) 对象的类型.`interface Key<out M : `[`Message`](./index.md)`>` |

### Functions
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [contentEquals](content-equals.md) | 判断内容是否与 [another](content-equals.md#net.mamoe.mirai.message.data.Message$contentEquals(net.mamoe.mirai.message.data.Message, kotlin.Boolean)/another) 相等.`open fun contentEquals(another: `[`Message`](./index.md)`, ignoreCase: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>`open fun contentEquals(another: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, ignoreCase: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [contentToString](content-to-string.md) | 转为最接近官方格式的字符串. 如 `At(member) + "test"` 将转为 `"@群名片 test"`.`abstract fun contentToString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [followedBy](followed-by.md) | 将 `this` 和 [tail](followed-by.md#net.mamoe.mirai.message.data.Message$followedBy(net.mamoe.mirai.message.data.Message)/tail) 连接.`open fun followedBy(tail: `[`Message`](./index.md)`): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [plus](plus.md) | `open operator fun plus(another: `[`MessageChain`](../-message-chain/index.md)`): `[`MessageChain`](../-message-chain/index.md)<br>`open operator fun plus(another: `[`Message`](./index.md)`): `[`MessageChain`](../-message-chain/index.md)<br>`open operator fun plus(another: `[`SingleMessage`](../-single-message.md)`): `[`MessageChain`](../-message-chain/index.md)<br>`open operator fun plus(another: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageChain`](../-message-chain/index.md)<br>`open operator fun plus(another: `[`CharSequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`): `[`MessageChain`](../-message-chain/index.md)<br>`open operator fun plus(another: `[`Iterable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)`<`[`Message`](./index.md)`>): `[`MessageChain`](../-message-chain/index.md)<br>`open operator fun plus(another: `[`Iterable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>): `[`MessageChain`](../-message-chain/index.md)<br>`open operator fun plus(another: `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`Message`](./index.md)`>): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toString](to-string.md) | 得到包含 mirai 消息元素代码的, 易读的字符串. 如 `At(member) + "test"` 将转为 `"[mirai:at:qqId]test"``abstract fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Properties
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [content](../content.md) | [Message.contentToString](content-to-string.md) 的捷径`val `[`Message`](./index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [asMessageChain](../as-message-chain.md) | 得到包含 [this](../as-message-chain/-this-.md) 的 [MessageChain](../-message-chain/index.md).`fun `[`Message`](./index.md)`.asMessageChain(): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [flatten](../flatten.md) | 扁平化 [Message](./index.md)`fun `[`Message`](./index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](../-single-message.md)`>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isContentEmpty](../is-content-empty.md) | 判断消息内容是否为空.`fun `[`Message`](./index.md)`.isContentEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isContentNotEmpty](../is-content-not-empty.md) | `fun `[`Message`](./index.md)`.isContentNotEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isNotPlain](../is-not-plain.md) | `fun `[`Message`](./index.md)`.isNotPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isPlain](../is-plain.md) | `fun `[`Message`](./index.md)`.isPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [plus](../plus.md) | `suspend operator fun `[`Message`](./index.md)`.plus(another: Flow<`[`Message`](./index.md)`>): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [repeat](../repeat.md) | 将此消息元素按顺序重复 [count](../repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](./index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sendTo](../send-to.md) | `suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](./index.md)`.sendTo(contact: C): `[`MessageReceipt`](../../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [times](../times.md) | 将此消息元素按顺序重复 [count](../times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](./index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toForwardMessage](../to-forward-message.md) | 转换为 [ForwardMessage](../-forward-message/index.md)`fun `[`Message`](./index.md)`.toForwardMessage(sender: `[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md)<br>`fun `[`Message`](./index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md) |

### Inheritors
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Image](../-image/index.md) | 自定义表情 (收藏的表情) 和普通图片.`interface Image : `[`Message`](./index.md)`, `[`MessageContent`](../-message-content.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MessageChain](../-message-chain/index.md) | 消息链. 空的实现为 [EmptyMessageChain](../-empty-message-chain/index.md)`interface MessageChain : `[`Message`](./index.md)`, `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`SingleMessage`](../-single-message.md)`>, `[`RandomAccess`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-random-access.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MessageSource](../-message-source/index.md) | 消息源, 它存在于 [MessageChain](../-message-chain/index.md) 中, 用于表示这个消息的来源.`sealed class MessageSource : `[`Message`](./index.md)`, `[`MessageMetadata`](../-message-metadata/index.md)`, `[`ConstrainSingle`](../-constrain-single/index.md)`<`[`MessageSource`](../-message-source/index.md)`>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [QuoteReply](../-quote-reply/index.md) | 引用回复.`class QuoteReply : `[`Message`](./index.md)`, `[`MessageMetadata`](../-message-metadata/index.md)`, `[`ConstrainSingle`](../-constrain-single/index.md)`<`[`QuoteReply`](../-quote-reply/index.md)`>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SingleMessage](../-single-message.md) | 单个消息元素. 与之相对的是 [MessageChain](../-message-chain/index.md), 是多个 [SingleMessage](../-single-message.md) 的集合.`interface SingleMessage : `[`Message`](./index.md) |

