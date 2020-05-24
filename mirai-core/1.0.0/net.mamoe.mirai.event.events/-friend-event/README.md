[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [FriendEvent](./index.md)

# FriendEvent

`interface FriendEvent : `[`BotEvent`](../-bot-event/index.md)

有关好友的事件

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |
| [friend](friend.md) | `abstract val friend: `[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |

### Inheritors

| Name | Summary |
|---|---|
| [FriendAddEvent](../-friend-add-event/index.md) | 成功添加了一个新好友的事件`data class FriendAddEvent : `[`FriendEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [FriendAvatarChangedEvent](../-friend-avatar-changed-event/index.md) | [Friend](../../net.mamoe.mirai.contact/-friend/index.md) 头像被修改. 在此事件广播前就已经修改完毕.`data class FriendAvatarChangedEvent : `[`FriendEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [FriendDeleteEvent](../-friend-delete-event/index.md) | 好友已被删除的事件.`data class FriendDeleteEvent : `[`FriendEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [FriendRemarkChangeEvent](../-friend-remark-change-event/index.md) | 好友昵称改变事件. 目前仅支持解析 (来自 PC 端的修改).`data class FriendRemarkChangeEvent : `[`FriendEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
