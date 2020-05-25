[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [MemberJoinRequestEvent](./index.md)

# MemberJoinRequestEvent

`data class MemberJoinRequestEvent : `[`BotEvent`](../-bot-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

一个账号请求加入群事件, [Bot](../../net.mamoe.mirai/-bot/index.md) 在此群中是管理员或群主.

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |
| [eventId](event-id.md) | 事件唯一识别号`val eventId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [fromId](from-id.md) | 申请入群的账号的 id`val fromId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [fromNick](from-nick.md) | 申请人昵称`val fromNick: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [group](group.md) | `val group: `[`Group`](../../net.mamoe.mirai.contact/-group/index.md) |
| [groupId](group-id.md) | `val groupId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [groupName](group-name.md) | `val groupName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [message](message.md) | 入群申请消息`val message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Functions

| Name | Summary |
|---|---|
| [__acceptBlockingForJava__](__accept-blocking-for-java__.md) | `fun __acceptBlockingForJava__(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [__ignoreBlockingForJava__](__ignore-blocking-for-java__.md) | `fun __ignoreBlockingForJava__(blackList: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [__rejectBlockingForJava__](__reject-blocking-for-java__.md) | `fun __rejectBlockingForJava__(blackList: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [accept](accept.md) | `suspend fun accept(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [ignore](ignore.md) | `suspend fun ignore(blackList: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [reject](reject.md) | `suspend fun reject(blackList: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
