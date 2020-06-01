[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotLeaveEvent](./index.md)

# BotLeaveEvent

`sealed class BotLeaveEvent : `[`BotEvent`](../-bot-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

机器人被踢出群或在其他客户端主动退出一个群. 在事件广播前 [Bot.groups](../../net.mamoe.mirai/-bot/groups.md) 就已删除这个群.

### Types

| Name | Summary |
|---|---|
| [Active](-active/index.md) | 机器人主动退出一个群.`data class Active : `[`BotLeaveEvent`](./index.md) |
| [Kick](-kick/index.md) | 机器人被管理员或群主踢出群.`data class Kick : `[`BotLeaveEvent`](./index.md)`, `[`GroupOperableEvent`](../-group-operable-event/index.md) |

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `open val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |
| [group](group.md) | `abstract val group: `[`Group`](../../net.mamoe.mirai.contact/-group/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
