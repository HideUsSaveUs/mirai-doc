[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [MessageSendEvent](./index.md)

# MessageSendEvent

`sealed class MessageSendEvent : `[`BotEvent`](../-bot-event/index.md)`, `[`BotActiveEvent`](../-bot-active-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

主动发送消息

**See Also**

[Contact.sendMessage](../../net.mamoe.mirai.contact/-contact/send-message.md)

### Types

| Name | Summary |
|---|---|
| [FriendMessageSendEvent](-friend-message-send-event/index.md) | `data class FriendMessageSendEvent : `[`MessageSendEvent`](./index.md)`, `[`CancellableEvent`](../../net.mamoe.mirai.event/-cancellable-event/index.md) |
| [GroupMessageSendEvent](-group-message-send-event/index.md) | `data class GroupMessageSendEvent : `[`MessageSendEvent`](./index.md)`, `[`CancellableEvent`](../../net.mamoe.mirai.event/-cancellable-event/index.md) |
| [TempMessageSendEvent](-temp-message-send-event/index.md) | `data class TempMessageSendEvent : `[`MessageSendEvent`](./index.md)`, `[`CancellableEvent`](../../net.mamoe.mirai.event/-cancellable-event/index.md) |

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |
| [target](target.md) | `abstract val target: `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
