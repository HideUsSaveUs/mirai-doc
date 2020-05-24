[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [FriendAddEvent](./index.md)

# FriendAddEvent

`data class FriendAddEvent : `[`FriendEvent`](../-friend-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

成功添加了一个新好友的事件

### Properties

| Name | Summary |
|---|---|
| [friend](friend.md) | 新好友. 已经添加到 [Bot.friends](../../net.mamoe.mirai/-bot/friends.md)`val friend: `[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
