[mirai-core](../../index.md) / [net.mamoe.mirai.event.events](../index.md) / [BeforeImageUploadEvent](./index.md)

# BeforeImageUploadEvent

`data class BeforeImageUploadEvent : `[`BotEvent`](../-bot-event/index.md)`, `[`BotActiveEvent`](../-bot-active-event.md)`, `[`AbstractEvent`](../../net.mamoe.mirai.event/-abstract-event/index.md)`, `[`CancellableEvent`](../../net.mamoe.mirai.event/-cancellable-event/index.md)

图片上传前. 可以阻止上传.

此事件总是在 [ImageUploadEvent](../-image-upload-event/index.md) 之前广播.
若此事件被取消, [ImageUploadEvent](../-image-upload-event/index.md) 不会广播.

**See Also**

[Contact.uploadImage](../../net.mamoe.mirai.contact/-contact/upload-image.md)

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../net.mamoe.mirai/-bot/index.md) |
| [source](source.md) | `val source: `[`ExternalImage`](../../net.mamoe.mirai.utils/-external-image/index.md) |
| [target](target.md) | `val target: `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../../net.mamoe.mirai.event/__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../../net.mamoe.mirai.event/broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../../net.mamoe.mirai.event/-event/index.md)`> E.broadcast(): E` |
