[mirai-core](../index.md) / [net.mamoe.mirai.message.data](./index.md)

## Package net.mamoe.mirai.message.data

### Types

| Name | Summary |
|---|---|
| [At](-at/index.md) | At 一个群成员. 只能发送给一个群.`data class At : `[`MessageContent`](-message-content.md) |
| [AtAll](-at-all/index.md) | "@全体成员".`object AtAll : Key<`[`AtAll`](-at-all/index.md)`>, `[`MessageContent`](-message-content.md) |
| [ConstrainSingle](-constrain-single/index.md) | 约束一个 [MessageChain](-message-chain/index.md) 中只存在这一种类型的元素. 新元素将会替换旧元素, 保持原顺序.`interface ConstrainSingle<out M : `[`Message`](-message/index.md)`> : `[`MessageMetadata`](-message-metadata/index.md) |
| [CustomMessage](-custom-message/index.md) | 自定义消息`sealed class CustomMessage : `[`SingleMessage`](-single-message.md) |
| [CustomMessageMetadata](-custom-message-metadata/index.md) | 自定义消息元数据.`abstract class CustomMessageMetadata : `[`CustomMessage`](-custom-message/index.md)`, `[`MessageMetadata`](-message-metadata/index.md) |
| [EmptyMessageChain](-empty-message-chain/index.md) | 不含任何元素的 [MessageChain](-message-chain/index.md).`object EmptyMessageChain : `[`MessageChain`](-message-chain/index.md)`, `[`Iterator`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)`<`[`SingleMessage`](-single-message.md)`>, `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`SingleMessage`](-single-message.md)`>` |
| [Face](-face/index.md) | QQ 自带表情`data class Face : `[`MessageContent`](-message-content.md) |
| [FlashImage](-flash-image/index.md) | 闪照`sealed class FlashImage : `[`MessageContent`](-message-content.md)`, `[`HummerMessage`](-hummer-message/index.md) |
| [ForwardMessage](-forward-message/index.md) | 合并转发消息`class ForwardMessage : `[`MessageContent`](-message-content.md) |
| [ForwardMessageBuilder](-forward-message-builder/index.md) | 转发消息 DSL 构建器.`class ForwardMessageBuilder : `[`MutableList`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)`<INode>` |
| [FriendFlashImage](-friend-flash-image/index.md) | `data class FriendFlashImage : `[`FlashImage`](-flash-image/index.md) |
| [FriendImage](-friend-image/index.md) | 好友图片`sealed class FriendImage : AbstractImage` |
| [GroupFlashImage](-group-flash-image/index.md) | `data class GroupFlashImage : `[`FlashImage`](-flash-image/index.md) |
| [GroupImage](-group-image/index.md) | 群图片.`sealed class GroupImage : AbstractImage` |
| [HummerMessage](-hummer-message/index.md) | 一些特殊的消息`sealed class HummerMessage : `[`MessageContent`](-message-content.md) |
| [Image](-image/index.md) | 自定义表情 (收藏的表情) 和普通图片.`interface Image : `[`Message`](-message/index.md)`, `[`MessageContent`](-message-content.md) |
| [LightApp](-light-app/index.md) | 小程序, 如音乐分享.`data class LightApp : `[`RichMessage`](-rich-message/index.md) |
| [Message](-message/index.md) | 可发送的或从服务器接收的消息.`interface Message` |
| [MessageChain](-message-chain/index.md) | 消息链. 空的实现为 [EmptyMessageChain](-empty-message-chain/index.md)`interface MessageChain : `[`Message`](-message/index.md)`, `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`SingleMessage`](-single-message.md)`>, `[`RandomAccess`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-random-access.html) |
| [MessageChainBuilder](-message-chain-builder/index.md) | [MessageChain](-message-chain/index.md) 构建器. 多个连续的 [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) 会被连接为单个 [PlainText](-plain-text/index.md) 以优化性能.`open class MessageChainBuilder : `[`MutableList`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)`<`[`SingleMessage`](-single-message.md)`>, `[`Appendable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.text/-appendable/index.html) |
| [MessageContent](-message-content.md) | 消息内容`interface MessageContent : `[`SingleMessage`](-single-message.md) |
| [MessageMetadata](-message-metadata/index.md) | 消息元数据, 即不含内容的元素.`interface MessageMetadata : `[`SingleMessage`](-single-message.md) |
| [MessageSource](-message-source/index.md) | 消息源, 它存在于 [MessageChain](-message-chain/index.md) 中, 用于表示这个消息的来源.`sealed class MessageSource : `[`Message`](-message/index.md)`, `[`MessageMetadata`](-message-metadata/index.md)`, `[`ConstrainSingle`](-constrain-single/index.md)`<`[`MessageSource`](-message-source/index.md)`>` |
| [MessageSourceAmender](-message-source-amender/index.md) | 仅于 [copyAmend](copy-amend.md) 中修改 [MessageSource](-message-source/index.md)`interface MessageSourceAmender` |
| [MessageSourceBuilder](-message-source-builder/index.md) | `abstract class MessageSourceBuilder` |
| [OfflineMessageSource](-offline-message-source/index.md) | 由一条消息中的 [QuoteReply](-quote-reply/index.md) 得到的 [MessageSource](-message-source/index.md). 此消息源可能来自一条与机器人无关的消息. 因此无法提供对象化的 `sender` 或 `target` 获取.`abstract class OfflineMessageSource : `[`MessageSource`](-message-source/index.md) |
| [OnlineMessageSource](-online-message-source/index.md) | 在线消息的 [MessageSource](-message-source/index.md). 拥有对象化的 [sender](-online-message-source/sender.md), [target](-online-message-source/target.md), 也可以直接 [recall](recall.md) 和 [quote](quote.md)`sealed class OnlineMessageSource : `[`MessageSource`](-message-source/index.md) |
| [OrNullDelegate](-or-null-delegate/index.md) | 可空的委托`class OrNullDelegate<out R : `[`Message`](-message/index.md)`?>` |
| [PlainText](-plain-text/index.md) | 纯文本. 可含 emoji 表情如 😊.`data class PlainText : `[`MessageContent`](-message-content.md) |
| [PokeMessage](-poke-message/index.md) | 戳一戳. 可以发送给好友或群.`data class PokeMessage : `[`HummerMessage`](-hummer-message/index.md) |
| [PttMessage](-ptt-message/index.md) | 需要通过上传到服务器的消息，如语音、文件`abstract class PttMessage : `[`MessageContent`](-message-content.md) |
| [QuoteReply](-quote-reply/index.md) | 引用回复.`class QuoteReply : `[`Message`](-message/index.md)`, `[`MessageMetadata`](-message-metadata/index.md)`, `[`ConstrainSingle`](-constrain-single/index.md)`<`[`QuoteReply`](-quote-reply/index.md)`>` |
| [RichMessage](-rich-message/index.md) | XML, JSON 消息等富文本消息`interface RichMessage : `[`MessageContent`](-message-content.md) |
| [ServiceMessage](-service-message/index.md) | 服务消息, 可以是 JSON 消息或 XML 消息.`open class ServiceMessage : `[`RichMessage`](-rich-message/index.md) |
| [SingleMessage](-single-message.md) | 单个消息元素. 与之相对的是 [MessageChain](-message-chain/index.md), 是多个 [SingleMessage](-single-message.md) 的集合.`interface SingleMessage : `[`Message`](-message/index.md) |
| [VipFace](-vip-face/index.md) | VIP 表情.`data class VipFace : `[`HummerMessage`](-hummer-message/index.md) |
| [Voice](-voice/index.md) | 语音消息, 目前只支持接收和转发`class Voice : `[`PttMessage`](-ptt-message/index.md) |

### Annotations

| Name | Summary |
|---|---|
| [ForwardMessageDsl](-forward-message-dsl/index.md) | 标记转发消息 DSL`annotation class ForwardMessageDsl` |
| [XmlMessageDsl](-xml-message-dsl/index.md) | `annotation class XmlMessageDsl` |

### Extensions for External Classes

| Name | Summary |
|---|---|
| [kotlin.Array](kotlin.-array/index.md) |  |
| [kotlin.collections.Collection](kotlin.collections.-collection/index.md) |  |
| [kotlin.collections.Iterable](kotlin.collections.-iterable/index.md) |  |
| [kotlin.sequences.Sequence](kotlin.sequences.-sequence/index.md) |  |
| [kotlin.String](kotlin.-string/index.md) |  |

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | 消息内部 id. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](-message-chain/index.md)`.bot: `[`Bot`](../net.mamoe.mirai/-bot/index.md)`val `[`QuoteReply`](-quote-reply/index.md)`.bot: `[`Bot`](../net.mamoe.mirai/-bot/index.md) |
| [content](content.md) | [Message.contentToString](-message/content-to-string.md) 的捷径`val `[`Message`](-message/index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [FRIEND_IMAGE_ID_REGEX_1](-f-r-i-e-n-d_-i-m-a-g-e_-i-d_-r-e-g-e-x_1.md) | 好友图片 ID 正则表达式`val FRIEND_IMAGE_ID_REGEX_1: `[`Regex`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.text/-regex/index.html) |
| [FRIEND_IMAGE_ID_REGEX_2](-f-r-i-e-n-d_-i-m-a-g-e_-i-d_-r-e-g-e-x_2.md) | 好友图片 ID 正则表达式 2`val FRIEND_IMAGE_ID_REGEX_2: `[`Regex`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.text/-regex/index.html) |
| [GROUP_IMAGE_ID_REGEX](-g-r-o-u-p_-i-m-a-g-e_-i-d_-r-e-g-e-x.md) | 群图片 ID 正则表达式`val GROUP_IMAGE_ID_REGEX: `[`Regex`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.text/-regex/index.html) |
| [id](id.md) | 消息 id. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](-message-chain/index.md)`.id: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [internalId](internal-id.md) | 消息内部 id. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](-message-chain/index.md)`.internalId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [md5](md5.md) | 计算图片的 md5 校验值.`val `[`Image`](-image/index.md)`.md5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) |
| [source](source.md) | 获取这条消息源 仅从服务器接收的消息才可以获取消息源`val `[`MessageChain`](-message-chain/index.md)`.source: `[`MessageSource`](-message-source/index.md) |
| [time](time.md) | 消息时间. 仅从服务器接收的消息才可以获取`val `[`MessageChain`](-message-chain/index.md)`.time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |

### Functions

| Name | Summary |
|---|---|
| [_____newChain______](_____new-chain______.md) | 构造一个 [MessageChain](-message-chain/index.md) 为提供更好的 Java API.`fun _____newChain______(messages: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`MessageChain`](-message-chain/index.md) |
| [allContent](all-content.md) | 如果每一个 [消息内容](-message-content.md) 都满足 [block](all-content.md#net.mamoe.mirai.message.data$allContent(net.mamoe.mirai.message.data.MessageChain, kotlin.Function1((net.mamoe.mirai.message.data.MessageContent, kotlin.Boolean)))/block), 返回 `true``fun `[`MessageChain`](-message-chain/index.md)`.allContent(block: (`[`MessageContent`](-message-content.md)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [any](any.md) | 获取第一个 [M](any.md#M) 类型的 [Message](-message/index.md) 实例`fun <M : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.any(key: Key<M>): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [anyIsInstance](any-is-instance.md) | 判断 [this](any-is-instance/-this-.md) 中是否存在 [Message](-message/index.md) 的实例`fun <M : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.anyIsInstance(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [asMessageChain](as-message-chain.md) | 得到包含 [this](as-message-chain/-this-.md) 的 [MessageChain](-message-chain/index.md).`fun `[`Message`](-message/index.md)`.asMessageChain(): `[`MessageChain`](-message-chain/index.md)<br>直接将 [this](as-message-chain/-this-.md) 委托为一个 [MessageChain](-message-chain/index.md)`fun `[`SingleMessage`](-single-message.md)`.asMessageChain(): `[`MessageChain`](-message-chain/index.md)`fun `[`MessageChain`](-message-chain/index.md)`.asMessageChain(): `[`MessageChain`](-message-chain/index.md) |
| [at](at.md) | At 这个成员`fun `[`Member`](../net.mamoe.mirai.contact/-member/index.md)`.at(): `[`At`](-at/index.md) |
| [buildForwardMessage](build-forward-message.md) | 构造一条 [ForwardMessage](-forward-message/index.md)`fun buildForwardMessage(context: `[`Contact`](../net.mamoe.mirai.contact/-contact/index.md)`, displayStrategy: DisplayStrategy = DisplayStrategy, block: `[`ForwardMessageBuilder`](-forward-message-builder/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`ForwardMessage`](-forward-message/index.md)<br>使用 DSL 构建一个 [ForwardMessage](-forward-message/index.md).`fun `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`.buildForwardMessage(context: `[`Contact`](../net.mamoe.mirai.contact/-contact/index.md)` = this.subject, displayStrategy: DisplayStrategy = DisplayStrategy, block: `[`ForwardMessageBuilder`](-forward-message-builder/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`ForwardMessage`](-forward-message/index.md) |
| [buildMessageChain](build-message-chain.md) | 构建一个 [MessageChain](-message-chain/index.md)`fun buildMessageChain(block: `[`MessageChainBuilder`](-message-chain-builder/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`MessageChain`](-message-chain/index.md)<br>使用特定的容器大小构建一个 [MessageChain](-message-chain/index.md)`fun buildMessageChain(initialSize: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, block: `[`MessageChainBuilder`](-message-chain-builder/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`MessageChain`](-message-chain/index.md) |
| [buildMessageSource](build-message-source.md) | 构建一个 [OfflineMessageSource](-offline-message-source/index.md)`fun `[`Bot`](../net.mamoe.mirai/-bot/index.md)`.buildMessageSource(block: `[`MessageSourceBuilder`](-message-source-builder/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`MessageSource`](-message-source/index.md) |
| [copyAmend](copy-amend.md) | 复制这个消息源, 并以 [block](copy-amend.md#net.mamoe.mirai.message.data$copyAmend(net.mamoe.mirai.message.data.MessageSource, kotlin.Function1((net.mamoe.mirai.message.data.MessageSourceAmender, kotlin.Unit)))/block) 修改`fun `[`MessageSource`](-message-source/index.md)`.copyAmend(block: `[`MessageSourceAmender`](-message-source-amender/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`OfflineMessageSource`](-offline-message-source/index.md) |
| [first](first.md) | 获取第一个 [M](first.md#M) 类型的 [Message](-message/index.md) 实例`fun <M : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.first(key: Key<M>): M` |
| [firstIsInstance](first-is-instance.md) | 获取第一个 [M](first-is-instance.md#M) 类型的 [Message](-message/index.md) 实例`fun <M : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.firstIsInstance(): M` |
| [firstIsInstanceOrNull](first-is-instance-or-null.md) | 获取第一个 [M](first-is-instance-or-null.md#M) 类型的 [Message](-message/index.md) 实例`fun <M : `[`Message`](-message/index.md)`?> `[`MessageChain`](-message-chain/index.md)`.firstIsInstanceOrNull(): M?` |
| [firstOrNull](first-or-null.md) | 获取第一个 [M](first-or-null.md#M) 类型的 [Message](-message/index.md) 实例`fun <M : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.firstOrNull(key: Key<M>): M?` |
| [flash](flash.md) | `fun `[`Image`](-image/index.md)`.flash(): `[`FlashImage`](-flash-image/index.md)<br>`fun `[`GroupImage`](-group-image/index.md)`.flash(): `[`GroupFlashImage`](-group-flash-image/index.md)<br>`fun `[`FriendImage`](-friend-image/index.md)`.flash(): `[`FriendFlashImage`](-friend-flash-image/index.md) |
| [flatten](flatten.md) | 扁平化 [Message](-message/index.md)`fun `[`Message`](-message/index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](-single-message.md)`>``fun `[`MessageChain`](-message-chain/index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](-single-message.md)`>` |
| [forEachContent](for-each-content.md) | 遍历每一个 [消息内容](-message-content.md)`fun `[`MessageChain`](-message-chain/index.md)`.forEachContent(block: (`[`MessageContent`](-message-content.md)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [getOrFail](get-or-fail.md) | 获取第一个类型为 [key](get-or-fail.md#net.mamoe.mirai.message.data$getOrFail(net.mamoe.mirai.message.data.MessageChain, net.mamoe.mirai.message.data.Message.Key((net.mamoe.mirai.message.data.getOrFail.M)), kotlin.Function1((net.mamoe.mirai.message.data.Message.Key((net.mamoe.mirai.message.data.getOrFail.M)), kotlin.String)))/key) 的 [Message](-message/index.md) 实例`fun <M : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.getOrFail(key: Key<M>, lazyMessage: (key: Key<M>) -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = { key.typeName }): M` |
| [getValue](get-value.md) | 提供一个类型的值的委托. 若不存在则会抛出异常 [NoSuchElementException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-no-such-element-exception/index.html)`operator fun <T : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.getValue(thisRef: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?, property: `[`KProperty`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-property/index.html)`<*>): T` |
| [Image](-image.md) | 通过 [Image.imageId](-image/image-id.md) 构造一个 [Image](-image/index.md) 以便发送. 这个图片必须是服务器已经存在的图片. 图片 id 不一定会长时间保存, 因此不建议使用 id 发送图片.`fun Image(imageId: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): OfflineImage` |
| [isAboutFriend](is-about-friend.md) | 判断是否是发送给好友, 或从好友接收的消息的消息源`fun `[`MessageSource`](-message-source/index.md)`.isAboutFriend(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isAboutGroup](is-about-group.md) | 判断是否是发送给群, 或从群接收的消息的消息源`fun `[`MessageSource`](-message-source/index.md)`.isAboutGroup(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isAboutTemp](is-about-temp.md) | 判断是否是发送给临时会话, 或从临时会话接收的消息的消息源`fun `[`MessageSource`](-message-source/index.md)`.isAboutTemp(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isContentEmpty](is-content-empty.md) | 判断消息内容是否为空.`fun `[`Message`](-message/index.md)`.isContentEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isContentNotEmpty](is-content-not-empty.md) | `fun `[`Message`](-message/index.md)`.isContentNotEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isNotPlain](is-not-plain.md) | `fun `[`Message`](-message/index.md)`.isNotPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isPlain](is-plain.md) | `fun `[`Message`](-message/index.md)`.isPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [messageChainOf](message-chain-of.md) | 返回一个包含 [messages](message-chain-of.md#net.mamoe.mirai.message.data$messageChainOf(kotlin.Array((net.mamoe.mirai.message.data.Message)))/messages) 所有元素的消息链, 保留顺序.`fun messageChainOf(vararg messages: `[`Message`](-message/index.md)`): `[`MessageChain`](-message-chain/index.md) |
| [noneContent](none-content.md) | 如果每一个 [消息内容](-message-content.md) 都不满足 [block](none-content.md#net.mamoe.mirai.message.data$noneContent(net.mamoe.mirai.message.data.MessageChain, kotlin.Function1((net.mamoe.mirai.message.data.MessageContent, kotlin.Boolean)))/block), 返回 `true``fun `[`MessageChain`](-message-chain/index.md)`.noneContent(block: (`[`MessageContent`](-message-content.md)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [orElse](or-else.md) | 提供一个类型的 [Message](-message/index.md) 的委托, 若不存在这个类型的 [Message](-message/index.md) 则委托会提供 `null``fun <T : `[`Message`](-message/index.md)`?> `[`MessageChain`](-message-chain/index.md)`.orElse(lazyDefault: () -> T): `[`OrNullDelegate`](-or-null-delegate/index.md)`<T>` |
| [orNull](or-null.md) | 提供一个类型的 [Message](-message/index.md) 的委托, 若不存在这个类型的 [Message](-message/index.md) 则委托会提供 `null``fun <T : `[`Message`](-message/index.md)`> `[`MessageChain`](-message-chain/index.md)`.orNull(): `[`OrNullDelegate`](-or-null-delegate/index.md)`<T?>` |
| [plus](plus.md) | `suspend operator fun `[`Message`](-message/index.md)`.plus(another: Flow<`[`Message`](-message/index.md)`>): `[`MessageChain`](-message-chain/index.md) |
| [queryUrl](query-url.md) | 查询原图下载链接.`suspend fun `[`Image`](-image/index.md)`.queryUrl(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [quote](quote.md) | 引用这条消息`fun `[`MessageSource`](-message-source/index.md)`.quote(): `[`QuoteReply`](-quote-reply/index.md)<br>引用这条消息. 仅从服务器接收的消息 (即来自 [MessageEvent](../net.mamoe.mirai.message/-message-event/index.md)) 才可以通过这个方式被引用.`fun `[`MessageChain`](-message-chain/index.md)`.quote(): `[`QuoteReply`](-quote-reply/index.md) |
| [recall](recall.md) | 撤回这条消息. 可撤回自己 2 分钟内发出的消息, 和任意时间的群成员的消息.`suspend fun `[`MessageSource`](-message-source/index.md)`.recall(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`suspend fun `[`MessageChain`](-message-chain/index.md)`.recall(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [recallIn](recall-in.md) | 在一段时间后撤回这条消息. 可撤回自己 2 分钟内发出的消息, 和任意时间的群成员的消息.`fun `[`MessageSource`](-message-source/index.md)`.recallIn(timeMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): Job`<br>`fun `[`MessageChain`](-message-chain/index.md)`.recallIn(millis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): Job` |
| [recallSource](recall-source.md) | 撤回引用的源消息`suspend fun `[`QuoteReply`](-quote-reply/index.md)`.recallSource(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [recallSourceIn](recall-source-in.md) | 在一段时间后撤回引用的源消息`fun `[`QuoteReply`](-quote-reply/index.md)`.recallSourceIn(millis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)` = EmptyCoroutineContext): Job` |
| [repeat](repeat.md) | 将此消息元素按顺序重复 [count](repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](-message/index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](-message-chain/index.md) |
| [sendTo](send-to.md) | 将 [this](send-to/-this-.md) 发送给指定联系人`suspend fun <C : `[`Contact`](../net.mamoe.mirai.contact/-contact/index.md)`> `[`MessageChain`](-message-chain/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../net.mamoe.mirai.message/-message-receipt/index.md)`<C>``suspend fun <C : `[`Contact`](../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](-message/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` |
| [times](times.md) | 将此消息元素按顺序重复 [count](times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](-message/index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](-message-chain/index.md) |
| [toForwardMessage](to-forward-message.md) | 转换为 [ForwardMessage](-forward-message/index.md)`fun `[`Message`](-message/index.md)`.toForwardMessage(sender: `[`User`](../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](-forward-message/index.md)<br>`fun `[`Message`](-message/index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](-forward-message/index.md) |
| [toOffline](to-offline.md) | 将在线消息源转换为离线消息源.`fun `[`OnlineMessageSource`](-online-message-source/index.md)`.toOffline(): `[`OfflineMessageSource`](-offline-message-source/index.md) |
