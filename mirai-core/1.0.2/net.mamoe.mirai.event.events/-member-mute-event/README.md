[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [MemberMuteEvent](./index.md)

# MemberMuteEvent

`data class MemberMuteEvent : `[`GroupMemberEvent`](../-group-member-event/index.md)`, Packet, `[`GroupOperableEvent`](../-group-operable-event/index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

群成员被禁言事件. 被禁言的成员都不可能是机器人本人

**See Also**

[BotMuteEvent](../-bot-mute-event/index.md)

### Properties

| Name | Summary |
|---|---|
| [durationSeconds](duration-seconds.md) | `val durationSeconds: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [member](member.md) | `val member: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md) |
| [operator](operator.md) | 操作人. 为 null 则为机器人操作`val operator: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md)`?` |

### Extension Properties

| Name | Summary |
|---|---|
| [isByBot](../is-by-bot.md) | 是否由 [Bot](../../net.mamoe.mirai/-bot/index.md) 操作`val `[`GroupOperableEvent`](../-group-operable-event/index.md)`.isByBot: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [operatorOrBot](../operator-or-bot.md) | 当操作人为 [Member](../../net.mamoe.mirai.contact/-member/index.md) 时获取这个 [Member](../../net.mamoe.mirai.contact/-member/index.md), 当操作人为 [Bot](../../net.mamoe.mirai/-bot/index.md) 时获取 [Group.botAsMember](../../net.mamoe.mirai.contact/-group/bot-as-member.md)`val `[`GroupOperableEvent`](../-group-operable-event/index.md)`.operatorOrBot: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
