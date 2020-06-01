[mirai-core](../../index.md) / [net.mamoe.mirai](../index.md) / [Bot](./index.md)

# Bot

`abstract class Bot : CoroutineScope, `[`LowLevelBotAPIAccessor`](../-low-level-bot-a-p-i-accessor/index.md)`, BotJavaFriendlyAPI, `[`ContactOrBot`](../../net.mamoe.mirai.contact/-contact-or-bot/index.md)

机器人对象. 一个机器人实例登录一个 QQ 账号.
Mirai 为多账号设计, 可同时维护多个机器人.

有关 [Bot](./index.md) 生命管理, 请查看 [BotConfiguration.inheritCoroutineContext](../../net.mamoe.mirai.utils/-bot-configuration/inherit-coroutine-context.md)

**See Also**

[Contact](../../net.mamoe.mirai.contact/-contact/index.md)

[kotlinx.coroutines.isActive](#)

[BotFactory](../-bot-factory/index.md)

### Properties

| Name | Summary |
|---|---|
| [configuration](configuration.md) | `val configuration: `[`BotConfiguration`](../../net.mamoe.mirai.utils/-bot-configuration/index.md) |
| [context](context.md) | [Bot](./index.md) 运行的 [Context](../../net.mamoe.mirai.utils/-context/index.md).`abstract val context: `[`Context`](../../net.mamoe.mirai.utils/-context/index.md) |
| [coroutineContext](coroutine-context.md) | `val coroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) |
| [friends](friends.md) | 机器人的好友列表. 与服务器同步更新`abstract val friends: `[`ContactList`](../../net.mamoe.mirai.contact/-contact-list/index.md)`<`[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md)`>` |
| [groups](groups.md) | 机器人加入的群列表. 与服务器同步更新`abstract val groups: `[`ContactList`](../../net.mamoe.mirai.contact/-contact-list/index.md)`<`[`Group`](../../net.mamoe.mirai.contact/-group/index.md)`>` |
| [id](id.md) | QQ 号码. 实际类型为 uint`abstract val id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [isOnline](is-online.md) | 判断 Bot 是否在线 (可正常收发消息)`abstract val isOnline: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [logger](logger.md) | 日志记录器`abstract val logger: `[`MiraiLogger`](../../net.mamoe.mirai.utils/-mirai-logger/index.md) |
| [nick](nick.md) | 昵称`abstract val nick: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [selfQQ](self-q-q.md) | [User.id](../../net.mamoe.mirai.contact/-user/id.md) 与 [Bot.id](id.md) 相同的 [_lowLevelNewFriend](../-low-level-bot-a-p-i-accessor/_low-level-new-friend.md) 实例`abstract val selfQQ: `[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md) |

### Functions

| Name | Summary |
|---|---|
| [close](close.md) | 关闭这个 [Bot](./index.md), 立即取消 [Bot](./index.md) 的 [kotlinx.coroutines.SupervisorJob](#). 之后 [kotlinx.coroutines.isActive](#) 将会返回 `false`.`abstract fun close(cause: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`? = null): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [constructMessageSource](construct-message-source.md) | 构造一个 [OfflineMessageSource](../../net.mamoe.mirai.message.data/-offline-message-source/index.md)`abstract fun constructMessageSource(kind: Kind, fromUin: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, targetUin: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, id: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, internalId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, originalMessage: `[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md)`): `[`OfflineMessageSource`](../../net.mamoe.mirai.message.data/-offline-message-source/index.md) |
| [getFriend](get-friend.md) | 获取一个好友对象.`fun getFriend(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md) |
| [getGroup](get-group.md) | 获取一个机器人加入的群.`fun getGroup(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Group`](../../net.mamoe.mirai.contact/-group/index.md) |
| [login](login.md) | 登录, 或重新登录. 这个函数总是关闭一切现有网路任务 (但不会关闭其他任务), 然后重新登录并重新缓存好友列表和群列表.`abstract suspend fun login(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [recall](recall.md) | 撤回这条消息. 可撤回自己 2 分钟内发出的消息, 和任意时间的群成员的消息.`abstract suspend fun recall(source: `[`MessageSource`](../../net.mamoe.mirai.message.data/-message-source/index.md)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [toString](to-string.md) | `fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Companion Object Properties

| Name | Summary |
|---|---|
| [botInstances](bot-instances.md) | 复制一份此时的 [Bot](./index.md) 实例列表.`val botInstances: `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`Bot`](./index.md)`>` |
| [botInstancesSequence](bot-instances-sequence.md) | 复制一份此时的 [Bot](./index.md) 实例列表.`val botInstancesSequence: `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`Bot`](./index.md)`>` |

### Companion Object Functions

| Name | Summary |
|---|---|
| [forEachInstance](for-each-instance.md) | 遍历每一个 [Bot](./index.md) 实例`fun forEachInstance(block: (`[`Bot`](./index.md)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [getInstance](get-instance.md) | 获取一个 [Bot](./index.md) 实例, 无对应实例时抛出 [NoSuchElementException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-no-such-element-exception/index.html)`fun getInstance(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Bot`](./index.md) |
| [getInstanceOrNull](get-instance-or-null.md) | 获取一个 [Bot](./index.md) 实例, 无对应实例时返回 `null``fun getInstanceOrNull(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Bot`](./index.md)`?` |

### Extension Properties

| Name | Summary |
|---|---|
| [supervisorJob](../supervisor-job.md) | 获取 [Job](#) 的协程 [Job](#). 此 [Job](#) 为一个 [SupervisorJob](#)`val `[`Bot`](./index.md)`.supervisorJob: CompletableJob` |

### Extension Functions

| Name | Summary |
|---|---|
| [alsoLogin](../also-login.md) | 登录, 返回 [this](../also-login/-this-.md)`suspend fun <B : `[`Bot`](./index.md)`> B.alsoLogin(): B` |
| [buildMessageSource](../../net.mamoe.mirai.message.data/build-message-source.md) | 构建一个 [OfflineMessageSource](../../net.mamoe.mirai.message.data/-offline-message-source/index.md)`fun `[`Bot`](./index.md)`.buildMessageSource(block: `[`MessageSourceBuilder`](../../net.mamoe.mirai.message.data/-message-source-builder/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`MessageSource`](../../net.mamoe.mirai.message.data/-message-source/index.md) |
| [closeAndJoin](../close-and-join.md) | 关闭这个 [Bot](./index.md), 停止一切相关活动. 所有引用都会被释放.`suspend fun `[`Bot`](./index.md)`.closeAndJoin(cause: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`? = null): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [containsFriend](../contains-friend.md) | `fun `[`Bot`](./index.md)`.containsFriend(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [containsGroup](../contains-group.md) | `fun `[`Bot`](./index.md)`.containsGroup(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [getFriendOrNull](../get-friend-or-null.md) | `fun `[`Bot`](./index.md)`.getFriendOrNull(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md)`?` |
| [getGroupOrNull](../get-group-or-null.md) | `fun `[`Bot`](./index.md)`.getGroupOrNull(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Group`](../../net.mamoe.mirai.contact/-group/index.md)`?` |
| [join](../join.md) | 挂起协程直到 [Bot](./index.md) 协程被关闭 ([Bot.close](close.md)). 即使 [Bot](./index.md) 离线, 也会等待直到协程关闭.`suspend fun `[`Bot`](./index.md)`.join(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [recall](../recall.md) | 撤回这条消息.`suspend fun `[`Bot`](./index.md)`.recall(message: `[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
