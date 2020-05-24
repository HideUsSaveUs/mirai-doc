[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [MessageChain](./index.md)

# MessageChain

`interface MessageChain : `[`Message`](../-message/index.md)`, `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`SingleMessage`](../-single-message.md)`>, `[`RandomAccess`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-random-access.html)

消息链. 空的实现为 [EmptyMessageChain](../-empty-message-chain/index.md)

要获取更多消息相关的信息, 查看 [Message](../-message/index.md)

### 构造消息链

*
*
* [asMessageChain](../as-message-chain.md) 将 [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html), [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html) 等类型消息转换为 [MessageChain](./index.md)
* [messageChainOf](../message-chain-of.md) 类似 [listOf](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/list-of.html), 将多个 [Message](../-message/index.md) 构造为 [MessageChain](./index.md)

**See Also**

[get](get.md)

[getOrFail](../get-or-fail.md)

[quote](../quote.md)

[recall](../recall.md)

[buildMessageChain](../build-message-chain.md)

[asMessageChain](../as-message-chain.md)

[asMessageChain](../as-message-chain.md)

[forEachContent](../for-each-content.md)

[allContent](../all-content.md)

[noneContent](../none-content.md)

[orNull](../or-null.md)

[orElse](../or-else.md)

[getValue](../get-value.md)

[flatten](../kotlin.collections.-iterable/flatten.md)

### Properties
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [size](size.md) | 元素数量. [EmptyMessageChain](../-empty-message-chain/index.md) 不参加计数.`abstract val size: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |

### Functions
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [__forEachContentForJava__](__for-each-content-for-java__.md) | 遍历每一个有内容的消息, 即 [At](../-at/index.md), [AtAll](../-at-all/index.md), [PlainText](../-plain-text/index.md), [Image](../-image/index.md), [Face](../-face/index.md) 等 仅供 `Java` 使用`fun __forEachContentForJava__(block: (`[`Message`](../-message/index.md)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [get](get.md) | 获取第一个类型为 [key](get.md#net.mamoe.mirai.message.data.MessageChain$get(net.mamoe.mirai.message.data.Message.Key((net.mamoe.mirai.message.data.MessageChain.get.M)))/key) 的 [Message](../-message/index.md) 实例. 若不存在此实例, 返回 `null``operator fun <M : `[`Message`](../-message/index.md)`> get(key: Key<M>): M?` |

### Extension Properties
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [bot](../bot.md) | 消息内部 id. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](./index.md)`.bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [content](../content.md) | [Message.contentToString](../-message/content-to-string.md) 的捷径`val `[`Message`](../-message/index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [id](../id.md) | 消息 id. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](./index.md)`.id: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [internalId](../internal-id.md) | 消息内部 id. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](./index.md)`.internalId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [source](../source.md) | 获取这条消息源 仅从服务器接收的消息才可以获取消息源`val `[`MessageChain`](./index.md)`.source: `[`MessageSource`](../-message-source/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [time](../time.md) | 消息时间. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](./index.md)`.time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |

### Extension Functions
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allContent](../all-content.md) | 如果每一个 [消息内容](../-message-content.md) 都满足 [block](../all-content.md#net.mamoe.mirai.message.data$allContent(net.mamoe.mirai.message.data.MessageChain, kotlin.Function1((net.mamoe.mirai.message.data.MessageContent, kotlin.Boolean)))/block), 返回 `true``fun `[`MessageChain`](./index.md)`.allContent(block: (`[`MessageContent`](../-message-content.md)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [any](../any.md) | 获取第一个 [M](../any.md#M) 类型的 [Message](../-message/index.md) 实例`fun <M : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.any(key: Key<M>): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [anyIsInstance](../any-is-instance.md) | 判断 [this](../any-is-instance/-this-.md) 中是否存在 [Message](../-message/index.md) 的实例`fun <M : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.anyIsInstance(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [asMessageChain](../as-message-chain.md) | `fun `[`MessageChain`](./index.md)`.asMessageChain(): `[`MessageChain`](./index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [first](../first.md) | 获取第一个 [M](../first.md#M) 类型的 [Message](../-message/index.md) 实例`fun <M : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.first(key: Key<M>): M` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [firstIsInstance](../first-is-instance.md) | 获取第一个 [M](../first-is-instance.md#M) 类型的 [Message](../-message/index.md) 实例`fun <M : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.firstIsInstance(): M` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [firstIsInstanceOrNull](../first-is-instance-or-null.md) | 获取第一个 [M](../first-is-instance-or-null.md#M) 类型的 [Message](../-message/index.md) 实例`fun <M : `[`Message`](../-message/index.md)`?> `[`MessageChain`](./index.md)`.firstIsInstanceOrNull(): M?` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [firstOrNull](../first-or-null.md) | 获取第一个 [M](../first-or-null.md#M) 类型的 [Message](../-message/index.md) 实例`fun <M : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.firstOrNull(key: Key<M>): M?` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [flatten](../flatten.md) | `fun `[`MessageChain`](./index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](../-single-message.md)`>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [forEachContent](../for-each-content.md) | 遍历每一个 [消息内容](../-message-content.md)`fun `[`MessageChain`](./index.md)`.forEachContent(block: (`[`MessageContent`](../-message-content.md)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [getOrFail](../get-or-fail.md) | 获取第一个类型为 [key](../get-or-fail.md#net.mamoe.mirai.message.data$getOrFail(net.mamoe.mirai.message.data.MessageChain, net.mamoe.mirai.message.data.Message.Key((net.mamoe.mirai.message.data.getOrFail.M)), kotlin.Function1((net.mamoe.mirai.message.data.Message.Key((net.mamoe.mirai.message.data.getOrFail.M)), kotlin.String)))/key) 的 [Message](../-message/index.md) 实例`fun <M : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.getOrFail(key: Key<M>, lazyMessage: (key: Key<M>) -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = { key.typeName }): M` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [getValue](../get-value.md) | 提供一个类型的值的委托. 若不存在则会抛出异常 [NoSuchElementException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-no-such-element-exception/index.html)`operator fun <T : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.getValue(thisRef: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?, property: `[`KProperty`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-property/index.html)`<*>): T` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isContentEmpty](../is-content-empty.md) | 判断消息内容是否为空.`fun `[`Message`](../-message/index.md)`.isContentEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isContentNotEmpty](../is-content-not-empty.md) | `fun `[`Message`](../-message/index.md)`.isContentNotEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isNotPlain](../is-not-plain.md) | `fun `[`Message`](../-message/index.md)`.isNotPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isPlain](../is-plain.md) | `fun `[`Message`](../-message/index.md)`.isPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [noneContent](../none-content.md) | 如果每一个 [消息内容](../-message-content.md) 都不满足 [block](../none-content.md#net.mamoe.mirai.message.data$noneContent(net.mamoe.mirai.message.data.MessageChain, kotlin.Function1((net.mamoe.mirai.message.data.MessageContent, kotlin.Boolean)))/block), 返回 `true``fun `[`MessageChain`](./index.md)`.noneContent(block: (`[`MessageContent`](../-message-content.md)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [orElse](../or-else.md) | 提供一个类型的 [Message](../-message/index.md) 的委托, 若不存在这个类型的 [Message](../-message/index.md) 则委托会提供 `null``fun <T : `[`Message`](../-message/index.md)`?> `[`MessageChain`](./index.md)`.orElse(lazyDefault: () -> T): `[`OrNullDelegate`](../-or-null-delegate/index.md)`<T>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [orNull](../or-null.md) | 提供一个类型的 [Message](../-message/index.md) 的委托, 若不存在这个类型的 [Message](../-message/index.md) 则委托会提供 `null``fun <T : `[`Message`](../-message/index.md)`> `[`MessageChain`](./index.md)`.orNull(): `[`OrNullDelegate`](../-or-null-delegate/index.md)`<T?>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [plus](../plus.md) | `suspend operator fun `[`Message`](../-message/index.md)`.plus(another: Flow<`[`Message`](../-message/index.md)`>): `[`MessageChain`](./index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [quote](../quote.md) | 引用这条消息. 仅从服务器接收的消息 (即来自 [MessageEvent](../../net.mamoe.mirai.message/-message-event/index.md)) 才可以通过这个方式被引用.`fun `[`MessageChain`](./index.md)`.quote(): `[`QuoteReply`](../-quote-reply/index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [recall](../recall.md) | 撤回这条消息. 可撤回自己 2 分钟内发出的消息, 和任意时间的群成员的消息.`suspend fun `[`MessageChain`](./index.md)`.recall(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [recallIn](../recall-in.md) | 在一段时间后撤回这条消息. 可撤回自己 2 分钟内发出的消息, 和任意时间的群成员的消息.`fun `[`MessageChain`](./index.md)`.recallIn(millis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): Job` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [repeat](../repeat.md) | 将此消息元素按顺序重复 [count](../repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](../-message/index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](./index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sendTo](../send-to.md) | 将 [this](../send-to/-this-.md) 发送给指定联系人`suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`MessageChain`](./index.md)`.sendTo(contact: C): `[`MessageReceipt`](../../net.mamoe.mirai.message/-message-receipt/index.md)`<C>``suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](../-message/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [times](../times.md) | 将此消息元素按顺序重复 [count](../times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](../-message/index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](./index.md) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toForwardMessage](../to-forward-message.md) | 转换为 [ForwardMessage](../-forward-message/index.md)`fun `[`Message`](../-message/index.md)`.toForwardMessage(sender: `[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md)<br>`fun `[`Message`](../-message/index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](../-forward-message/index.md) |

### Inheritors
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EmptyMessageChain](../-empty-message-chain/index.md) | 不含任何元素的 [MessageChain](./index.md).`object EmptyMessageChain : `[`MessageChain`](./index.md)`, `[`Iterator`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)`<`[`SingleMessage`](../-single-message.md)`>, `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`SingleMessage`](../-single-message.md)`>` |

