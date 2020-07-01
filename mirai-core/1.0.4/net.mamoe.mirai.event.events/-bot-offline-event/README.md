[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotOfflineEvent](./index.md)

# BotOfflineEvent

`sealed class BotOfflineEvent : `[`BotEvent`](../-bot-event/index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)

[Bot](../../net.mamoe.mirai/-bot/index.md) 离线.

### Types

| Name | Summary |
|---|---|
| [Active](-active/index.md) | 主动离线. 主动广播这个事件也可以让 [Bot](../../net.mamoe.mirai/-bot/index.md) 关闭.`data class Active : `[`BotOfflineEvent`](./index.md)`, `[`BotActiveEvent`](../-bot-active-event.md)`, CauseAware` |
| [CauseAware](-cause-aware/index.md) | `interface CauseAware` |
| [Dropped](-dropped/index.md) | 因网络问题而掉线`data class Dropped : `[`BotOfflineEvent`](./index.md)`, Packet, `[`BotPassiveEvent`](../-bot-passive-event.md)`, CauseAware` |
| [Force](-force/index.md) | 被挤下线`data class Force : `[`BotOfflineEvent`](./index.md)`, Packet, `[`BotPassiveEvent`](../-bot-passive-event.md) |
| [MsfOffline](-msf-offline/index.md) | 被服务器断开`data class MsfOffline : `[`BotOfflineEvent`](./index.md)`, Packet, `[`BotPassiveEvent`](../-bot-passive-event.md)`, CauseAware` |
| [RequireReconnect](-require-reconnect/index.md) | 服务器主动要求更换另一个服务器`data class RequireReconnect : `[`BotOfflineEvent`](./index.md)`, Packet, `[`BotPassiveEvent`](../-bot-passive-event.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
