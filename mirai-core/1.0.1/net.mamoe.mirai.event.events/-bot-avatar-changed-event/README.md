[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotAvatarChangedEvent](./index.md)

# BotAvatarChangedEvent

`data class BotAvatarChangedEvent : `[`BotEvent`](../-bot-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

[Bot](../../net.mamoe.mirai/-bot/index.md) 头像被修改（通过其他客户端修改了头像）. 在此事件广播前就已经修改完毕.

**See Also**

[FriendAvatarChangedEvent](../-friend-avatar-changed-event/index.md)

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | [Bot](../../net.mamoe.mirai/-bot/index.md) 头像被修改（通过其他客户端修改了头像）. 在此事件广播前就已经修改完毕.`BotAvatarChangedEvent(bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md)`)` |

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
