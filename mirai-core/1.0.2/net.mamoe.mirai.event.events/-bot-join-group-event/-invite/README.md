[mirai-core](../../../index.md) / [net.mamoe.mirai.event.events](../../index.md) / [BotJoinGroupEvent](../index.md) / [Invite](./index.md)

# Invite

`data class Invite : `[`BotPassiveEvent`](../../-bot-passive-event.md)`, `[`GroupEvent`](../../-group-event/index.md)`, Packet, `[`AbstractEvent`](../../../net.mamoe.mirai.event/-abstract-event/index.md)

Bot 被一个群内的成员直接邀请加入了群.

此时服务器基于 Bot 的 QQ 设置自动同意了请求.

### Properties

| Name | Summary |
|---|---|
| [group](group.md) | `val group: `[`Group`](../../../net.mamoe.mirai.contact/-group/index.md) |
| [invitor](invitor.md) | 邀请人`val invitor: `[`Member`](../../../net.mamoe.mirai.contact/-member/index.md) |

### Functions

| Name | Summary |
|---|---|
| [toString](to-string.md) | `fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
