[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [MemberJoinEvent](./index.md)

# MemberJoinEvent

`sealed class MemberJoinEvent : `[`GroupMemberEvent`](../-group-member-event/index.md)`, `[`BotPassiveEvent`](../-bot-passive-event.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

成员已经加入群的事件

### Types

| Name | Summary |
|---|---|
| [Active](-active/index.md) | 成员主动加入群`data class Active : `[`MemberJoinEvent`](./index.md) |
| [Invite](-invite/index.md) | 被邀请加入群`data class Invite : `[`MemberJoinEvent`](./index.md) |

### Properties

| Name | Summary |
|---|---|
| [member](member.md) | `open val member: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
