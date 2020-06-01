[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [GroupOperableEvent](./index.md)

# GroupOperableEvent

`interface GroupOperableEvent : `[`GroupEvent`](../-group-event/index.md)

可由 [Member](../../net.mamoe.mirai.contact/-member/index.md) 或 [Bot](../../net.mamoe.mirai/-bot/index.md) 操作的事件

**See Also**

[isByBot](../is-by-bot.md)

[operatorOrBot](../operator-or-bot.md)

### Properties

| Name | Summary |
|---|---|
| [operator](operator.md) | 操作人, 为 `null` 时为 [Bot](../../net.mamoe.mirai/-bot/index.md) 操作`abstract val operator: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md)`?` |

### Extension Properties

| Name | Summary |
|---|---|
| [isByBot](../is-by-bot.md) | 是否由 [Bot](../../net.mamoe.mirai/-bot/index.md) 操作`val `[`GroupOperableEvent`](./index.md)`.isByBot: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [operatorOrBot](../operator-or-bot.md) | 当操作人为 [Member](../../net.mamoe.mirai.contact/-member/index.md) 时获取这个 [Member](../../net.mamoe.mirai.contact/-member/index.md), 当操作人为 [Bot](../../net.mamoe.mirai/-bot/index.md) 时获取 [Group.botAsMember](../../net.mamoe.mirai.contact/-group/bot-as-member.md)`val `[`GroupOperableEvent`](./index.md)`.operatorOrBot: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |

### Inheritors

| Name | Summary |
|---|---|
| [GroupAllowAnonymousChatEvent](../-group-allow-anonymous-chat-event/index.md) | 群 "匿名聊天" 功能状态改变. 此事件广播前修改就已经完成.`data class GroupAllowAnonymousChatEvent : `[`GroupSettingChangeEvent`](../-group-setting-change-event/index.md)`<`[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`>, Packet, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [GroupAllowMemberInviteEvent](../-group-allow-member-invite-event/index.md) | 群 "允许群员邀请好友加群" 功能状态改变. 此事件广播前修改就已经完成.`data class GroupAllowMemberInviteEvent : `[`GroupSettingChangeEvent`](../-group-setting-change-event/index.md)`<`[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`>, Packet, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [GroupEntranceAnnouncementChangeEvent](../-group-entrance-announcement-change-event/index.md) | 入群公告改变. 此事件广播前修改就已经完成.`data class GroupEntranceAnnouncementChangeEvent : `[`GroupSettingChangeEvent`](../-group-setting-change-event/index.md)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>, Packet, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [GroupMuteAllEvent](../-group-mute-all-event/index.md) | 群 "全员禁言" 功能状态改变. 此事件广播前修改就已经完成.`data class GroupMuteAllEvent : `[`GroupSettingChangeEvent`](../-group-setting-change-event/index.md)`<`[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`>, Packet, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [GroupNameChangeEvent](../-group-name-change-event/index.md) | 群名改变. 此事件广播前修改就已经完成.`data class GroupNameChangeEvent : `[`GroupSettingChangeEvent`](../-group-setting-change-event/index.md)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>, Packet, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberMuteEvent](../-member-mute-event/index.md) | 群成员被禁言事件. 被禁言的成员都不可能是机器人本人`data class MemberMuteEvent : `[`GroupMemberEvent`](../-group-member-event/index.md)`, Packet, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberSpecialTitleChangeEvent](../-member-special-title-change-event/index.md) | 成员群头衔改动. 一定为群主操作`data class MemberSpecialTitleChangeEvent : `[`GroupMemberEvent`](../-group-member-event/index.md)`, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberUnmuteEvent](../-member-unmute-event/index.md) | 群成员被取消禁言事件. 被禁言的成员都不可能是机器人本人`data class MemberUnmuteEvent : `[`GroupMemberEvent`](../-group-member-event/index.md)`, Packet, `[`GroupOperableEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
