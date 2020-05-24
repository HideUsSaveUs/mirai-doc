[mirai-core](../../../index.md) / [net.mamoe.mirai.event.events](../../index.md) / [BotLeaveEvent](../index.md) / [Kick](./index.md)

# Kick

`data class Kick : `[`BotLeaveEvent`](../index.md)`, `[`GroupOperableEvent`](../../-group-operable-event/index.md)

机器人被管理员或群主踢出群.

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../../net.mamoe.mirai/-bot/index.md) |
| [group](group.md) | `val group: `[`Group`](../../../net.mamoe.mirai.contact/-group/index.md) |
| [operator](operator.md) | 操作人, 为 `null` 时为 [Bot](../../../net.mamoe.mirai/-bot/index.md) 操作`val operator: `[`Member`](../../../net.mamoe.mirai.contact/-member/index.md) |

### Functions

| Name | Summary |
|---|---|
| [toString](to-string.md) | `fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
