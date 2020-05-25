[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [MemberCardChangeEvent](./index.md)

# MemberCardChangeEvent

`data class MemberCardChangeEvent : `[`GroupMemberEvent`](../-group-member-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

成员群名片改动. 此事件广播前修改就已经完成.

### Properties

| Name | Summary |
|---|---|
| [member](member.md) | `val member: `[`Member`](../../net.mamoe.mirai.contact/-member/index.md) |
| [new](new.md) | 修改后`val new: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [origin](origin.md) | 修改前`val origin: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
