[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [BroadcastControllable](./index.md)

# BroadcastControllable

`interface BroadcastControllable : `[`Event`](../-event/index.md)

可控制是否需要广播这个事件

### Properties

| Name | Summary |
|---|---|
| [shouldBroadcast](should-broadcast.md) | 返回 `false` 时将不会广播这个事件.`open val shouldBroadcast: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../-event/index.md)`> E.broadcast(): E` |

### Inheritors

| Name | Summary |
|---|---|
| [FriendMessageEvent](../../net.mamoe.mirai.message/-friend-message-event/index.md) | 机器人收到的好友消息的事件`class FriendMessageEvent : FriendMessage, `[`BroadcastControllable`](./index.md) |
| [GroupSettingChangeEvent](../../net.mamoe.mirai.event.events/-group-setting-change-event/index.md) | 群设置改变. 此事件广播前修改就已经完成.`interface GroupSettingChangeEvent<T> : `[`GroupEvent`](../../net.mamoe.mirai.event.events/-group-event/index.md)`, `[`BotPassiveEvent`](../../net.mamoe.mirai.event.events/-bot-passive-event.md)`, `[`BroadcastControllable`](./index.md) |
| [TempMessageEvent](../../net.mamoe.mirai.message/-temp-message-event/index.md) | 机器人收到的群临时会话消息的事件`class TempMessageEvent : TempMessage, `[`BroadcastControllable`](./index.md) |
