[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [MemberLeaveEvent](./index.md)

# MemberLeaveEvent

`sealed class MemberLeaveEvent : `[`GroupMemberEvent`](../-group-member-event/index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

成员已经离开群的事件. 在事件广播前成员就已经从 [Group.members](../../net.mamoe.mirai.contact/-group/members.md) 中删除

### Types

| Name | Summary |
|---|---|
| [Kick](-kick/index.md) | 成员被踢出群. 成员不可能是机器人自己.`data class Kick : `[`MemberLeaveEvent`](./index.md)`, Packet, `[`GroupOperableEvent`](../-group-operable-event/index.md) |
| [Quit](-quit/index.md) | 成员主动离开`data class Quit : `[`MemberLeaveEvent`](./index.md)`, Packet` |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
