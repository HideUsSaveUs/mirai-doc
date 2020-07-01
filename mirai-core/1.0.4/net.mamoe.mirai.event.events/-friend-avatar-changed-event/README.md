[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [FriendAvatarChangedEvent](./index.md)

# FriendAvatarChangedEvent

`data class FriendAvatarChangedEvent : `[`FriendEvent`](../-friend-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

[Friend](../../net.mamoe.mirai.contact/-friend/index.md) 头像被修改. 在此事件广播前就已经修改完毕.

### Properties

| Name | Summary |
|---|---|
| [friend](friend.md) | `val friend: `[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
