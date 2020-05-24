[mirai-core](../../../index.md) / [net.mamoe.mirai.event.events](../../index.md) / [MemberLeaveEvent](../index.md) / [Kick](./index.md)

# Kick

`data class Kick : `[`MemberLeaveEvent`](../index.md)`, Packet, `[`GroupOperableEvent`](../../-group-operable-event/index.md)

成员被踢出群. 成员不可能是机器人自己.

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | 成员被踢出群. 成员不可能是机器人自己.`Kick(member: `[`Member`](../../../net.mamoe.mirai.contact/-member/index.md)`, operator: `[`Member`](../../../net.mamoe.mirai.contact/-member/index.md)`?)` |

### Properties

| Name | Summary |
|---|---|
| [member](member.md) | `val member: `[`Member`](../../../net.mamoe.mirai.contact/-member/index.md) |
| [operator](operator.md) | 操作人. 为 null 则是机器人操作.`val operator: `[`Member`](../../../net.mamoe.mirai.contact/-member/index.md)`?` |

### Functions

| Name | Summary |
|---|---|
| [toString](to-string.md) | `fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
