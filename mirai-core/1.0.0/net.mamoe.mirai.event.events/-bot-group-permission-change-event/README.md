[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotGroupPermissionChangeEvent](./index.md)

# BotGroupPermissionChangeEvent

`data class BotGroupPermissionChangeEvent : `[`BotPassiveEvent`](../-bot-passive-event.md)`, `[`GroupEvent`](../-group-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

Bot 在群里的权限被改变. 操作人一定是群主

### Properties

| Name | Summary |
|---|---|
| [group](group.md) | `val group: `[`Group`](../../net.mamoe.mirai.contact/-group/index.md) |
| [new](new.md) | `val new: `[`MemberPermission`](../../net.mamoe.mirai.contact/-member-permission/index.md) |
| [origin](origin.md) | `val origin: `[`MemberPermission`](../../net.mamoe.mirai.contact/-member-permission/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
