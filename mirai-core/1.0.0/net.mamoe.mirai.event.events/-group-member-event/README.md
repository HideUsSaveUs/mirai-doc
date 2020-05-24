[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [GroupMemberEvent](./index.md)

# GroupMemberEvent

`interface GroupMemberEvent : `[`GroupEvent`](../-group-event/index.md)

有关群成员的事件

### Properties

| Name | Summary |
|---|---|
| [group](group.md) | `open val group: `[`Group`](../../net.mamoe.mirai.contact/-group/index.md) |
| [member](member.md) | `abstract val member: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |

### Inheritors

| Name | Summary |
|---|---|
| [MemberCardChangeEvent](../-member-card-change-event/index.md) | 成员群名片改动. 此事件广播前修改就已经完成.`data class MemberCardChangeEvent : `[`GroupMemberEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberJoinEvent](../-member-join-event/index.md) | 成员已经加入群的事件`sealed class MemberJoinEvent : `[`GroupMemberEvent`](./index.md)`, `[`BotPassiveEvent`](../-bot-passive-event.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberLeaveEvent](../-member-leave-event/index.md) | 成员已经离开群的事件. 在事件广播前成员就已经从 [Group.members](../../net.mamoe.mirai.contact/-group/members.md) 中删除`sealed class MemberLeaveEvent : `[`GroupMemberEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberMuteEvent](../-member-mute-event/index.md) | 群成员被禁言事件. 被禁言的成员都不可能是机器人本人`data class MemberMuteEvent : `[`GroupMemberEvent`](./index.md)`, Packet, `[`GroupOperableEvent`](../-group-operable-event/index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberPermissionChangeEvent](../-member-permission-change-event/index.md) | 成员权限改变的事件. 成员不可能是机器人自己.`data class MemberPermissionChangeEvent : `[`GroupMemberEvent`](./index.md)`, `[`BotPassiveEvent`](../-bot-passive-event.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberSpecialTitleChangeEvent](../-member-special-title-change-event/index.md) | 成员群头衔改动. 一定为群主操作`data class MemberSpecialTitleChangeEvent : `[`GroupMemberEvent`](./index.md)`, `[`GroupOperableEvent`](../-group-operable-event/index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberUnmuteEvent](../-member-unmute-event/index.md) | 群成员被取消禁言事件. 被禁言的成员都不可能是机器人本人`data class MemberUnmuteEvent : `[`GroupMemberEvent`](./index.md)`, Packet, `[`GroupOperableEvent`](../-group-operable-event/index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
