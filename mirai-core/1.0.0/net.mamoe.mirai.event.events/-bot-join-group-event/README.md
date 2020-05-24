[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotJoinGroupEvent](./index.md)

# BotJoinGroupEvent

`sealed class BotJoinGroupEvent : `[`GroupEvent`](../-group-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

Bot 成功加入了一个新群

### Types

| Name | Summary |
|---|---|
| [Active](-active/index.md) | 不确定. 可能是主动加入`data class Active : `[`BotPassiveEvent`](../-bot-passive-event.md)`, `[`GroupEvent`](../-group-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [Invite](-invite/index.md) | Bot 被一个群内的成员直接邀请加入了群.`data class Invite : `[`BotPassiveEvent`](../-bot-passive-event.md)`, `[`GroupEvent`](../-group-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |

### Properties

| Name | Summary |
|---|---|
| [group](group.md) | `abstract val group: `[`Group`](../../net.mamoe.mirai.contact/-group/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
