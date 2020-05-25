[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [CustomMessage](./index.md)

# CustomMessage

`sealed class CustomMessage : `[`SingleMessage`](../-single-message.md)

自定义消息

它不会显示在消息文本中, 也不会被其他客户端识别.
只有 mirai 才能识别这些消息.

目前在回复时无法通过 [originalMessage](#) 获取自定义类型消息

``` kotlin
//Unresolved: samples.CustomMessageIdentifier
```

**See Also**

[CustomMessageMetadata](../-custom-message-metadata/index.md)

### Types

| Name | Summary |
|---|---|
| [CustomMessageFullData](-custom-message-full-data/index.md) | `class CustomMessageFullData` |
| [Factory](-factory/index.md) | 序列化和反序列化此消息的工厂, 将会自动注册. 应实现为 `object`.`abstract class Factory<M : `[`CustomMessage`](./index.md)`> : Key<M>` |
| [JsonSerializerFactory](-json-serializer-factory/index.md) | 使用 [Json](#) 作为序列模式的 [Factory](-factory/index.md) 推荐在调试时使用此工厂`abstract class JsonSerializerFactory<M : `[`CustomMessage`](./index.md)`> : Factory<M>` |
| [Key](-key/index.md) | `companion object Key : Key<`[`CustomMessage`](./index.md)`>` |
| [ProtoBufSerializerFactory](-proto-buf-serializer-factory/index.md) | 使用 [ProtoBuf](#) 作为序列模式的 [Factory](-factory/index.md). 推荐使用此工厂`abstract class ProtoBufSerializerFactory<M : `[`CustomMessage`](./index.md)`> : Factory<M>` |

### Exceptions

| Name | Summary |
|---|---|
| [CustomMessageFullDataDeserializeInternalException](-custom-message-full-data-deserialize-internal-exception/index.md) | `class CustomMessageFullDataDeserializeInternalException : `[`RuntimeException`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-runtime-exception/index.html) |
| [CustomMessageFullDataDeserializeUserException](-custom-message-full-data-deserialize-user-exception/index.md) | `class CustomMessageFullDataDeserializeUserException : `[`RuntimeException`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-runtime-exception/index.html) |

### Functions

| Name | Summary |
|---|---|
| [getFactory](get-factory.md) | 获取这个消息的工厂`abstract fun getFactory(): Factory<out `[`CustomMessage`](./index.md)`>` |

### Companion Object Properties

| Name | Summary |
|---|---|
| [typeName](type-name.md) | 此 [Key](../-message/-key/index.md) 指代的 [Message](../-message/index.md) 类型名. 一般为 `class.simpleName`, 如 "QuoteReply", "PlainText"`val typeName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Properties

| Name | Summary |
|---|---|
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
| [repeat](../repeat.md) | 将此消息元素按顺序重复 [count](../repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](../-message/index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) |
| [sendTo](../send-to.md) | `suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](../-message/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` |
| [times](../times.md) | 将此消息元素按顺序重复 [count](../times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](../-message/index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) |
| [toForwardMessage](../to-forward-message.md) | 转换为 [ForwardMessage](../-forward-message/index.md)`fun `[`Message`](../-message/index.md)`.toForwardMessage(sender: `[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md)<br>`fun `[`Message`](../-message/index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md) |

### Inheritors

| Name | Summary |
|---|---|
| [CustomMessageMetadata](../-custom-message-metadata/index.md) | 自定义消息元数据.`abstract class CustomMessageMetadata : `[`CustomMessage`](./index.md)`, `[`MessageMetadata`](../-message-metadata/index.md) |
