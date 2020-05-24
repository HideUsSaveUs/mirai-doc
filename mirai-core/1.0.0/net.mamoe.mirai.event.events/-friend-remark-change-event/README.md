[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [FriendRemarkChangeEvent](./index.md)

# FriendRemarkChangeEvent

`data class FriendRemarkChangeEvent : `[`FriendEvent`](../-friend-event/index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

好友昵称改变事件. 目前仅支持解析 (来自 PC 端的修改).

### Properties

| Name | Summary |
|---|---|
| [friend](friend.md) | `val friend: `[`Friend`](../../net.mamoe.mirai.contact/-friend/index.md) |
| [newName](new-name.md) | `val newName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
