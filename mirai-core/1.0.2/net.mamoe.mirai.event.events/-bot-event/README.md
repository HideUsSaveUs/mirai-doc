[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BotEvent](./index.md)

# BotEvent

`interface BotEvent : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)

有关一个 [Bot](../../net.mamoe.mirai/-bot/index.md) 的事件

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `abstract val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |

### Inheritors

| Name | Summary |
|---|---|
| [BeforeImageUploadEvent](../-before-image-upload-event/index.md) | 图片上传前. 可以阻止上传.`data class BeforeImageUploadEvent : `[`BotEvent`](./index.md)`, `[`BotActiveEvent`](../-bot-active-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)`, `[`CancellableEvent`](../../net.mamoe.mirai.event/-cancellable-event/index.md) |
| [BotActiveEvent](../-bot-active-event.md) | 由 [Bot](../../net.mamoe.mirai/-bot/index.md) 主动发起的动作的事件`interface BotActiveEvent : `[`BotEvent`](./index.md) |
| [BotAvatarChangedEvent](../-bot-avatar-changed-event/index.md) | [Bot](../../net.mamoe.mirai/-bot/index.md) 头像被修改（通过其他客户端修改了头像）. 在此事件广播前就已经修改完毕.`data class BotAvatarChangedEvent : `[`BotEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [BotInvitedJoinGroupRequestEvent](../-bot-invited-join-group-request-event/index.md) | [Bot](../../net.mamoe.mirai/-bot/index.md) 被邀请加入一个群.`data class BotInvitedJoinGroupRequestEvent : `[`BotEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [BotLeaveEvent](../-bot-leave-event/index.md) | 机器人被踢出群或在其他客户端主动退出一个群. 在事件广播前 [Bot.groups](../../net.mamoe.mirai/-bot/groups.md) 就已删除这个群.`sealed class BotLeaveEvent : `[`BotEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [BotOfflineEvent](../-bot-offline-event/index.md) | [Bot](../../net.mamoe.mirai/-bot/index.md) 离线.`sealed class BotOfflineEvent : `[`BotEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [BotPassiveEvent](../-bot-passive-event.md) | [Bot](../../net.mamoe.mirai/-bot/index.md) 被动接收的事件. 这些事件可能与机器人有关`interface BotPassiveEvent : `[`BotEvent`](./index.md) |
| [BotReloginEvent](../-bot-relogin-event/index.md) | [Bot](../../net.mamoe.mirai/-bot/index.md) 主动或被动重新登录. 在此事件广播前就已经登录完毕.`data class BotReloginEvent : `[`BotEvent`](./index.md)`, `[`BotActiveEvent`](../-bot-active-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [FriendEvent](../-friend-event/index.md) | 有关好友的事件`interface FriendEvent : `[`BotEvent`](./index.md) |
| [GroupEvent](../-group-event/index.md) | 有关群的事件`interface GroupEvent : `[`BotEvent`](./index.md) |
| [ImageUploadEvent](../-image-upload-event/index.md) | 图片上传完成.`sealed class ImageUploadEvent : `[`BotEvent`](./index.md)`, `[`BotActiveEvent`](../-bot-active-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MemberJoinRequestEvent](../-member-join-request-event/index.md) | 一个账号请求加入群事件, [Bot](../../net.mamoe.mirai/-bot/index.md) 在此群中是管理员或群主.`data class MemberJoinRequestEvent : `[`BotEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MessageEvent](../../net.mamoe.mirai.message/-message-event/index.md) | 一个 (收到的) 消息事件.`abstract class MessageEvent : ContactMessage, `[`BotEvent`](./index.md)`, `[`MessageEventExtensions`](../../net.mamoe.mirai.message/-message-event-extensions/index.md)`<`[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`>` |
| [MessageRecallEvent](../-message-recall-event/index.md) | 消息撤回事件. 可是任意消息被任意人撤回.`sealed class MessageRecallEvent : `[`BotEvent`](./index.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [MessageSendEvent](../-message-send-event/index.md) | 主动发送消息`sealed class MessageSendEvent : `[`BotEvent`](./index.md)`, `[`BotActiveEvent`](../-bot-active-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
| [NewFriendRequestEvent](../-new-friend-request-event/index.md) | 一个账号请求添加机器人为好友的事件`data class NewFriendRequestEvent : `[`BotEvent`](./index.md)`, Packet, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md) |
