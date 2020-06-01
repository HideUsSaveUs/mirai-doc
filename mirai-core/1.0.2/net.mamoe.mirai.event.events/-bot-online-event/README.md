[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotOnlineEvent](./index.md)

# BotOnlineEvent

`data class BotOnlineEvent : `[`BotActiveEvent`](../-bot-active-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

[Bot](../../net.mamoe.mirai/-bot/index.md) 登录完成, 好友列表, 群组列表初始化完成

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
