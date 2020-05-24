[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotUnmuteEvent](./index.md)

# BotUnmuteEvent

`data class BotUnmuteEvent : `[`GroupEvent`](../-group-event/index.md)`, Packet, `[`BotPassiveEvent`](../-bot-passive-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

Bot 被取消禁言

### Properties

| Name | Summary |
|---|---|
| [group](group.md) | `val group: `[`Group`](../../net.mamoe.mirai.contact/-group/index.md) |
| [operator](operator.md) | 操作人.`val operator: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
