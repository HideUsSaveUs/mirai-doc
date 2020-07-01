[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [PokeMessage](./index.md)

# PokeMessage

`data class PokeMessage : `[`HummerMessage`](../-hummer-message/index.md)

戳一戳. 可以发送给好友或群.

**See Also**

[Types](-types/index.md)

### Types

| Name | Summary |
|---|---|
| [Types](-types/index.md) | `companion object Types : Key<`[`PokeMessage`](./index.md)`>` |

### Properties

| Name | Summary |
|---|---|
| [id](id.md) | `val id: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [name](name.md) | 仅 mirai, 显示的名称`val name: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [type](type.md) | `val type: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |

### Functions

| Name | Summary |
|---|---|
| [contentToString](content-to-string.md) | 转为最接近官方格式的字符串. 如 `At(member) + "test"` 将转为 `"@群名片 test"`.`fun contentToString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [toString](to-string.md) | 得到包含 mirai 消息元素代码的, 易读的字符串. 如 `At(member) + "test"` 将转为 `"[mirai:at:qqId]test"``fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Companion Object Properties

| Name | Summary |
|---|---|
| [BaoBeiQiu](-bao-bei-qiu.md) | 宝贝球 (SVIP)`val BaoBeiQiu: `[`PokeMessage`](./index.md) |
| [FangDaZhao](-fang-da-zhao.md) | 放大招`val FangDaZhao: `[`PokeMessage`](./index.md) |
| [GouYin](-gou-yin.md) | 勾引`val GouYin: `[`PokeMessage`](./index.md) |
| [Heartbroken](-heartbroken.md) | 心碎`val Heartbroken: `[`PokeMessage`](./index.md) |
| [JieYin](-jie-yin.md) | 结印 (SVIP)`val JieYin: `[`PokeMessage`](./index.md) |
| [Like](-like.md) | 点赞`val Like: `[`PokeMessage`](./index.md) |
| [Poke](-poke.md) | 戳一戳`val Poke: `[`PokeMessage`](./index.md) |
| [QiaoMen](-qiao-men.md) | 敲门 (SVIP)`val QiaoMen: `[`PokeMessage`](./index.md) |
| [RangNiPi](-rang-ni-pi.md) | 让你皮 (SVIP)`val RangNiPi: `[`PokeMessage`](./index.md) |
| [Rose](-rose.md) | 玫瑰花 (SVIP)`val Rose: `[`PokeMessage`](./index.md) |
| [ShouLei](-shou-lei.md) | 手雷 (SVIP)`val ShouLei: `[`PokeMessage`](./index.md) |
| [ShowLove](-show-love.md) | 比心`val ShowLove: `[`PokeMessage`](./index.md) |
| [SixSixSix](-six-six-six.md) | 666`val SixSixSix: `[`PokeMessage`](./index.md) |
| [SuiPing](-sui-ping.md) | 碎屏 (SVIP)`val SuiPing: `[`PokeMessage`](./index.md) |
| [typeName](type-name.md) | 此 [Key](../-message/-key/index.md) 指代的 [Message](../-message/index.md) 类型名. 一般为 `class.simpleName`, 如 "QuoteReply", "PlainText"`val typeName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [values](values.md) | 所有类型数组`val values: `[`Array`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)`<`[`PokeMessage`](./index.md)`>` |
| [ZhaoHuanShu](-zhao-huan-shu.md) | 召唤术 (SVIP)`val ZhaoHuanShu: `[`PokeMessage`](./index.md) |
| [ZhuaYiXia](-zhua-yi-xia.md) | 抓一下 (SVIP)`val ZhuaYiXia: `[`PokeMessage`](./index.md) |

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
