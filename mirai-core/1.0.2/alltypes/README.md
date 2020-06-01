

### All Types

| Name | Summary |
|---|---|
|

##### [net.mamoe.mirai.event.AbstractEvent](../net.mamoe.mirai.event/-abstract-event/index.md)

所有实现了 [Event](../net.mamoe.mirai.event/-event/index.md) 接口的类都应该继承的父类.


| (extensions in package net.mamoe.mirai.message.data)

##### [kotlin.Array](../net.mamoe.mirai.message.data/kotlin.-array/index.md)


|

##### [net.mamoe.mirai.message.data.At](../net.mamoe.mirai.message.data/-at/index.md)

At 一个群成员. 只能发送给一个群.


|

##### [net.mamoe.mirai.message.data.AtAll](../net.mamoe.mirai.message.data/-at-all/index.md)

"@全体成员".


|

##### [net.mamoe.mirai.event.events.BeforeImageUploadEvent](../net.mamoe.mirai.event.events/-before-image-upload-event/index.md)

图片上传前. 可以阻止上传.


|

##### [net.mamoe.mirai.Bot](../net.mamoe.mirai/-bot/index.md)

机器人对象. 一个机器人实例登录一个 QQ 账号.
Mirai 为多账号设计, 可同时维护多个机器人.


|

##### [net.mamoe.mirai.event.events.BotActiveEvent](../net.mamoe.mirai.event.events/-bot-active-event.md)

由 [Bot](../net.mamoe.mirai/-bot/index.md) 主动发起的动作的事件


|

##### [net.mamoe.mirai.event.events.BotAvatarChangedEvent](../net.mamoe.mirai.event.events/-bot-avatar-changed-event/index.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 头像被修改（通过其他客户端修改了头像）. 在此事件广播前就已经修改完毕.


|

##### [net.mamoe.mirai.utils.BotConfiguration](../net.mamoe.mirai.utils/-bot-configuration/index.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 配置.


|

##### [net.mamoe.mirai.event.events.BotEvent](../net.mamoe.mirai.event.events/-bot-event/index.md)

有关一个 [Bot](../net.mamoe.mirai/-bot/index.md) 的事件


|

##### [net.mamoe.mirai.BotFactory](../net.mamoe.mirai/-bot-factory/index.md)

构造 [Bot](../net.mamoe.mirai/-bot-factory/-bot.md) 的工厂. 这是 [Bot](../net.mamoe.mirai/-bot-factory/-bot.md) 唯一的构造方式.


|

##### [net.mamoe.mirai.event.events.BotGroupPermissionChangeEvent](../net.mamoe.mirai.event.events/-bot-group-permission-change-event/index.md)

Bot 在群里的权限被改变. 操作人一定是群主


|

##### [net.mamoe.mirai.event.events.BotInvitedJoinGroupRequestEvent](../net.mamoe.mirai.event.events/-bot-invited-join-group-request-event/index.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 被邀请加入一个群.


|

##### [net.mamoe.mirai.contact.BotIsBeingMutedException](../net.mamoe.mirai.contact/-bot-is-being-muted-exception/index.md)

发送消息时 bot 正处于被禁言状态时抛出的异常.


|

##### [net.mamoe.mirai.event.events.BotJoinGroupEvent](../net.mamoe.mirai.event.events/-bot-join-group-event/index.md)

Bot 成功加入了一个新群


|

##### [net.mamoe.mirai.event.events.BotLeaveEvent](../net.mamoe.mirai.event.events/-bot-leave-event/index.md)

机器人被踢出群或在其他客户端主动退出一个群. 在事件广播前 [Bot.groups](../net.mamoe.mirai/-bot/groups.md) 就已删除这个群.


|

##### [net.mamoe.mirai.event.events.BotMuteEvent](../net.mamoe.mirai.event.events/-bot-mute-event/index.md)

Bot 被禁言


|

##### [net.mamoe.mirai.event.events.BotOfflineEvent](../net.mamoe.mirai.event.events/-bot-offline-event/index.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 离线.


|

##### [net.mamoe.mirai.event.events.BotOnlineEvent](../net.mamoe.mirai.event.events/-bot-online-event/index.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 登录完成, 好友列表, 群组列表初始化完成


|

##### [net.mamoe.mirai.event.events.BotPassiveEvent](../net.mamoe.mirai.event.events/-bot-passive-event.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 被动接收的事件. 这些事件可能与机器人有关


|

##### [net.mamoe.mirai.event.events.BotReloginEvent](../net.mamoe.mirai.event.events/-bot-relogin-event/index.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 主动或被动重新登录. 在此事件广播前就已经登录完毕.


|

##### [net.mamoe.mirai.event.events.BotUnmuteEvent](../net.mamoe.mirai.event.events/-bot-unmute-event/index.md)

Bot 被取消禁言


|

##### [net.mamoe.mirai.event.BroadcastControllable](../net.mamoe.mirai.event/-broadcast-controllable/index.md)

可控制是否需要广播这个事件


| (extensions in package net.mamoe.mirai.message)

##### [java.awt.image.BufferedImage](../net.mamoe.mirai.message/java.awt.image.-buffered-image/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [java.awt.image.BufferedImage](../net.mamoe.mirai.utils/java.awt.image.-buffered-image/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [kotlinx.coroutines.io.ByteReadChannel](../net.mamoe.mirai.utils/kotlinx.coroutines.io.-byte-read-channel/index.md)


|

##### [net.mamoe.mirai.event.CancellableEvent](../net.mamoe.mirai.event/-cancellable-event/index.md)

可被取消的事件


| (extensions in package net.mamoe.mirai.message.data)

##### [kotlin.collections.Collection](../net.mamoe.mirai.message.data/kotlin.collections.-collection/index.md)


|

##### [net.mamoe.mirai.message.data.ConstrainSingle](../net.mamoe.mirai.message.data/-constrain-single/index.md)

约束一个 [MessageChain](../net.mamoe.mirai.message.data/-message-chain/index.md) 中只存在这一种类型的元素. 新元素将会替换旧元素, 保持原顺序.


|

##### [net.mamoe.mirai.contact.Contact](../net.mamoe.mirai.contact/-contact/index.md)

联系对象, 即可以与 [Bot](../net.mamoe.mirai/-bot/index.md) 互动的对象. 包含 [用户](../net.mamoe.mirai.contact/-user/index.md), 和 [群](../net.mamoe.mirai.contact/-group/index.md).


|

##### [net.mamoe.mirai.contact.ContactList](../net.mamoe.mirai.contact/-contact-list/index.md)

只读联系人列表, 无锁链表实现


|

##### [net.mamoe.mirai.contact.ContactOrBot](../net.mamoe.mirai.contact/-contact-or-bot/index.md)

拥有 [id](../net.mamoe.mirai.contact/-contact-or-bot/id.md) 的对象.
此为 [Contact](../net.mamoe.mirai.contact/-contact/index.md) 与 [Bot](../net.mamoe.mirai/-bot/index.md) 的唯一公共接口.


|

##### [net.mamoe.mirai.utils.Context](../net.mamoe.mirai.utils/-context/index.md)

On Android, typealias to `android.content.Context`
On JVM, empty class.


|

##### [net.mamoe.mirai.utils.ContextImpl](../net.mamoe.mirai.utils/-context-impl/index.md)


| (extensions in package net.mamoe.mirai)

##### [kotlinx.coroutines.CoroutineScope](../net.mamoe.mirai/kotlinx.coroutines.-coroutine-scope/index.md)


| (extensions in package net.mamoe.mirai.event)

##### [kotlinx.coroutines.CoroutineScope](../net.mamoe.mirai.event/kotlinx.coroutines.-coroutine-scope/index.md)


|

##### [net.mamoe.mirai.network.CustomLoginFailedException](../net.mamoe.mirai.network/-custom-login-failed-exception/index.md)

非 mirai 实现的异常


|

##### [net.mamoe.mirai.message.data.CustomMessage](../net.mamoe.mirai.message.data/-custom-message/index.md)

自定义消息


|

##### [net.mamoe.mirai.message.data.CustomMessageMetadata](../net.mamoe.mirai.message.data/-custom-message-metadata/index.md)

自定义消息元数据.


|

##### [net.mamoe.mirai.utils.DefaultLoginSolver](../net.mamoe.mirai.utils/-default-login-solver/index.md)

自动选择 [SwingSolver](../net.mamoe.mirai.utils/-swing-solver/index.md) 或 [StandardCharImageLoginSolver](../net.mamoe.mirai.utils/-standard-char-image-login-solver/index.md)


|

##### [net.mamoe.mirai.utils.DeviceInfo](../net.mamoe.mirai.utils/-device-info/index.md)

设备信息. 可通过继承 [SystemDeviceInfo](../net.mamoe.mirai.utils/-system-device-info/index.md) 来在默认的基础上修改


|

##### [net.mamoe.mirai.utils.DeviceInfoData](../net.mamoe.mirai.utils/-device-info-data/index.md)


|

##### [net.mamoe.mirai.utils.DirectoryLogger](../net.mamoe.mirai.utils/-directory-logger/index.md)

将日志写入('append')到特定文件夹中的文件. 每日日志独立保存.


| (extensions in package net.mamoe.mirai.utils)

##### [kotlin.time.Duration](../net.mamoe.mirai.utils/kotlin.time.-duration/index.md)


|

##### [net.mamoe.mirai.message.data.EmptyMessageChain](../net.mamoe.mirai.message.data/-empty-message-chain/index.md)

不含任何元素的 [MessageChain](../net.mamoe.mirai.message.data/-message-chain/index.md).


|

##### [net.mamoe.mirai.event.Event](../net.mamoe.mirai.event/-event/index.md)

可被监听的类, 可以是任何 class 或 object.


|

##### [net.mamoe.mirai.event.events.EventCancelledException](../net.mamoe.mirai.event.events/-event-cancelled-exception/index.md)


|

##### [net.mamoe.mirai.event.EventHandler](../net.mamoe.mirai.event/-event-handler/index.md)

标注一个函数为事件监听器.


|

##### [net.mamoe.mirai.event.EventPriority](../net.mamoe.mirai.event/-event-priority.md)


|

##### [net.mamoe.mirai.utils.ExternalImage](../net.mamoe.mirai.utils/-external-image/index.md)

外部图片. 图片数据还没有读取到内存.


|

##### [net.mamoe.mirai.message.data.Face](../net.mamoe.mirai.message.data/-face/index.md)

QQ 自带表情


| (extensions in package net.mamoe.mirai.message)

##### [java.io.File](../net.mamoe.mirai.message/java.io.-file/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [java.io.File](../net.mamoe.mirai.utils/java.io.-file/index.md)


|

##### [net.mamoe.mirai.utils.FileCacheStrategy](../net.mamoe.mirai.utils/-file-cache-strategy/index.md)

缓存策略.


|

##### [net.mamoe.mirai.message.data.FlashImage](../net.mamoe.mirai.message.data/-flash-image/index.md)

闪照


|

##### [net.mamoe.mirai.network.ForceOfflineException](../net.mamoe.mirai.network/-force-offline-exception/index.md)

当 [Bot](../net.mamoe.mirai/-bot/index.md) 被迫下线时抛出, 作为 [Job.cancel](#) 的 `cause`


|

##### [net.mamoe.mirai.message.data.ForwardMessage](../net.mamoe.mirai.message.data/-forward-message/index.md)

合并转发消息


|

##### [net.mamoe.mirai.message.data.ForwardMessageBuilder](../net.mamoe.mirai.message.data/-forward-message-builder/index.md)

转发消息 DSL 构建器.


|

##### [net.mamoe.mirai.message.data.ForwardMessageDsl](../net.mamoe.mirai.message.data/-forward-message-dsl/index.md)

标记转发消息 DSL


|

##### [net.mamoe.mirai.contact.Friend](../net.mamoe.mirai.contact/-friend/index.md)

代表一位好友.


|

##### [net.mamoe.mirai.event.events.FriendAddEvent](../net.mamoe.mirai.event.events/-friend-add-event/index.md)

成功添加了一个新好友的事件


|

##### [net.mamoe.mirai.event.events.FriendAvatarChangedEvent](../net.mamoe.mirai.event.events/-friend-avatar-changed-event/index.md)

[Friend](../net.mamoe.mirai.contact/-friend/index.md) 头像被修改. 在此事件广播前就已经修改完毕.


|

##### [net.mamoe.mirai.event.events.FriendDeleteEvent](../net.mamoe.mirai.event.events/-friend-delete-event/index.md)

好友已被删除的事件.


|

##### [net.mamoe.mirai.event.events.FriendEvent](../net.mamoe.mirai.event.events/-friend-event/index.md)

有关好友的事件


|

##### [net.mamoe.mirai.message.data.FriendFlashImage](../net.mamoe.mirai.message.data/-friend-flash-image/index.md)


|

##### [net.mamoe.mirai.message.data.FriendImage](../net.mamoe.mirai.message.data/-friend-image/index.md)

好友图片


|

##### [net.mamoe.mirai.data.FriendInfo](../net.mamoe.mirai.data/-friend-info/index.md)


|

##### [net.mamoe.mirai.message.FriendMessageEvent](../net.mamoe.mirai.message/-friend-message-event/index.md)

机器人收到的好友消息的事件


|

##### [net.mamoe.mirai.event.FriendMessageSubscribersBuilder](../net.mamoe.mirai.event/-friend-message-subscribers-builder.md)


|

##### [net.mamoe.mirai.event.events.FriendRemarkChangeEvent](../net.mamoe.mirai.event.events/-friend-remark-change-event/index.md)

好友昵称改变事件. 目前仅支持解析 (来自 PC 端的修改).


|

##### [net.mamoe.mirai.contact.Group](../net.mamoe.mirai.contact/-group/index.md)

群.


|

##### [net.mamoe.mirai.data.GroupActiveData](../net.mamoe.mirai.data/-group-active-data/index.md)

群统计信息


|

##### [net.mamoe.mirai.event.events.GroupAllowAnonymousChatEvent](../net.mamoe.mirai.event.events/-group-allow-anonymous-chat-event/index.md)

群 "匿名聊天" 功能状态改变. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.event.events.GroupAllowConfessTalkEvent](../net.mamoe.mirai.event.events/-group-allow-confess-talk-event/index.md)

群 "坦白说" 功能状态改变. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.event.events.GroupAllowMemberInviteEvent](../net.mamoe.mirai.event.events/-group-allow-member-invite-event/index.md)

群 "允许群员邀请好友加群" 功能状态改变. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.data.GroupAnnouncement](../net.mamoe.mirai.data/-group-announcement/index.md)


|

##### [net.mamoe.mirai.data.GroupAnnouncementList](../net.mamoe.mirai.data/-group-announcement-list/index.md)

群公告数据类
getGroupAnnouncementList时，如果page=1，那么你可以在inst里拿到一些置顶公告


|

##### [net.mamoe.mirai.data.GroupAnnouncementMsg](../net.mamoe.mirai.data/-group-announcement-msg/index.md)


|

##### [net.mamoe.mirai.data.GroupAnnouncementSettings](../net.mamoe.mirai.data/-group-announcement-settings/index.md)


|

##### [net.mamoe.mirai.event.events.GroupEntranceAnnouncementChangeEvent](../net.mamoe.mirai.event.events/-group-entrance-announcement-change-event/index.md)

入群公告改变. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.event.events.GroupEvent](../net.mamoe.mirai.event.events/-group-event/index.md)

有关群的事件


|

##### [net.mamoe.mirai.message.data.GroupFlashImage](../net.mamoe.mirai.message.data/-group-flash-image/index.md)


|

##### [net.mamoe.mirai.message.data.GroupImage](../net.mamoe.mirai.message.data/-group-image/index.md)

群图片.


|

##### [net.mamoe.mirai.data.GroupInfo](../net.mamoe.mirai.data/-group-info/index.md)

群资料.


|

##### [net.mamoe.mirai.event.events.GroupMemberEvent](../net.mamoe.mirai.event.events/-group-member-event/index.md)

有关群成员的事件


|

##### [net.mamoe.mirai.message.GroupMessageEvent](../net.mamoe.mirai.message/-group-message-event/index.md)

机器人收到的群消息的事件


|

##### [net.mamoe.mirai.event.GroupMessageSubscribersBuilder](../net.mamoe.mirai.event/-group-message-subscribers-builder.md)


|

##### [net.mamoe.mirai.event.events.GroupMuteAllEvent](../net.mamoe.mirai.event.events/-group-mute-all-event/index.md)

群 "全员禁言" 功能状态改变. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.event.events.GroupNameChangeEvent](../net.mamoe.mirai.event.events/-group-name-change-event/index.md)

群名改变. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.event.events.GroupOperableEvent](../net.mamoe.mirai.event.events/-group-operable-event/index.md)

可由 [Member](../net.mamoe.mirai.contact/-member/index.md) 或 [Bot](../net.mamoe.mirai/-bot/index.md) 操作的事件


|

##### [net.mamoe.mirai.event.events.GroupSettingChangeEvent](../net.mamoe.mirai.event.events/-group-setting-change-event/index.md)

群设置改变. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.contact.GroupSettings](../net.mamoe.mirai.contact/-group-settings/index.md)

群设置


|

##### [net.mamoe.mirai.message.data.HummerMessage](../net.mamoe.mirai.message.data/-hummer-message/index.md)

一些特殊的消息


|

##### [net.mamoe.mirai.message.data.Image](../net.mamoe.mirai.message.data/-image/index.md)

自定义表情 (收藏的表情) 和普通图片.


|

##### [net.mamoe.mirai.event.events.ImageUploadEvent](../net.mamoe.mirai.event.events/-image-upload-event/index.md)

图片上传完成.


| (extensions in package net.mamoe.mirai.message)

##### [kotlinx.io.core.Input](../net.mamoe.mirai.message/kotlinx.io.core.-input/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [kotlinx.io.core.Input](../net.mamoe.mirai.utils/kotlinx.io.core.-input/index.md)


| (extensions in package net.mamoe.mirai.message)

##### [java.io.InputStream](../net.mamoe.mirai.message/java.io.-input-stream/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [java.io.InputStream](../net.mamoe.mirai.utils/java.io.-input-stream/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [kotlin.Int](../net.mamoe.mirai.utils/kotlin.-int/index.md)


| (extensions in package net.mamoe.mirai.message.data)

##### [kotlin.collections.Iterable](../net.mamoe.mirai.message.data/kotlin.collections.-iterable/index.md)


|

##### [net.mamoe.mirai.message.data.LightApp](../net.mamoe.mirai.message.data/-light-app/index.md)

小程序, 如音乐分享.


|

##### [net.mamoe.mirai.event.Listener](../net.mamoe.mirai.event/-listener/index.md)

事件监听器.
由 [CoroutineScope.subscribe](../net.mamoe.mirai.event/kotlinx.coroutines.-coroutine-scope/subscribe.md) 等方法返回.


|

##### [net.mamoe.mirai.event.ListenerHost](../net.mamoe.mirai.event/-listener-host.md)

实现这个接口的对象可以通过 [EventHandler](../net.mamoe.mirai.event/-event-handler/index.md) 标注事件监听函数, 并通过 [registerEvents](../net.mamoe.mirai.event/register-events.md) 注册.


|

##### [net.mamoe.mirai.event.ListeningStatus](../net.mamoe.mirai.event/-listening-status/index.md)

订阅者的状态


|

##### [net.mamoe.mirai.network.LoginFailedException](../net.mamoe.mirai.network/-login-failed-exception/index.md)

在 [登录](../net.mamoe.mirai/-bot/login.md) 失败时抛出, 可正常地中断登录过程.


|

##### [net.mamoe.mirai.utils.LoginSolver](../net.mamoe.mirai.utils/-login-solver/index.md)

验证码, 设备锁解决器


|

##### [net.mamoe.mirai.LowLevelAPI](../net.mamoe.mirai/-low-level-a-p-i/index.md)

标示这个 API 是低级的 API.


|

##### [net.mamoe.mirai.LowLevelBotAPIAccessor](../net.mamoe.mirai/-low-level-bot-a-p-i-accessor/index.md)

[Bot](../net.mamoe.mirai/-bot/index.md) 相关协议层低级 API.


|

##### [net.mamoe.mirai.contact.Member](../net.mamoe.mirai.contact/-member/index.md)

代表一位群成员.


|

##### [net.mamoe.mirai.event.events.MemberCardChangeEvent](../net.mamoe.mirai.event.events/-member-card-change-event/index.md)

成员群名片改动. 此事件广播前修改就已经完成.


|

##### [net.mamoe.mirai.data.MemberInfo](../net.mamoe.mirai.data/-member-info/index.md)


|

##### [net.mamoe.mirai.event.events.MemberJoinEvent](../net.mamoe.mirai.event.events/-member-join-event/index.md)

成员已经加入群的事件


|

##### [net.mamoe.mirai.event.events.MemberJoinRequestEvent](../net.mamoe.mirai.event.events/-member-join-request-event/index.md)

一个账号请求加入群事件, [Bot](../net.mamoe.mirai/-bot/index.md) 在此群中是管理员或群主.


|

##### [net.mamoe.mirai.event.events.MemberLeaveEvent](../net.mamoe.mirai.event.events/-member-leave-event/index.md)

成员已经离开群的事件. 在事件广播前成员就已经从 [Group.members](../net.mamoe.mirai.contact/-group/members.md) 中删除


|

##### [net.mamoe.mirai.event.events.MemberMuteEvent](../net.mamoe.mirai.event.events/-member-mute-event/index.md)

群成员被禁言事件. 被禁言的成员都不可能是机器人本人


|

##### [net.mamoe.mirai.contact.MemberPermission](../net.mamoe.mirai.contact/-member-permission/index.md)

群成员的权限.


|

##### [net.mamoe.mirai.event.events.MemberPermissionChangeEvent](../net.mamoe.mirai.event.events/-member-permission-change-event/index.md)

成员权限改变的事件. 成员不可能是机器人自己.


|

##### [net.mamoe.mirai.event.events.MemberSpecialTitleChangeEvent](../net.mamoe.mirai.event.events/-member-special-title-change-event/index.md)

成员群头衔改动. 一定为群主操作


|

##### [net.mamoe.mirai.event.events.MemberUnmuteEvent](../net.mamoe.mirai.event.events/-member-unmute-event/index.md)

群成员被取消禁言事件. 被禁言的成员都不可能是机器人本人


|

##### [net.mamoe.mirai.message.data.Message](../net.mamoe.mirai.message.data/-message/index.md)

可发送的或从服务器接收的消息.


|

##### [net.mamoe.mirai.message.data.MessageChain](../net.mamoe.mirai.message.data/-message-chain/index.md)

消息链. 空的实现为 [EmptyMessageChain](../net.mamoe.mirai.message.data/-empty-message-chain/index.md)


|

##### [net.mamoe.mirai.message.data.MessageChainBuilder](../net.mamoe.mirai.message.data/-message-chain-builder/index.md)

[MessageChain](../net.mamoe.mirai.message.data/-message-chain/index.md) 构建器.
多个连续的 [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) 会被连接为单个 [PlainText](../net.mamoe.mirai.message.data/-plain-text/index.md) 以优化性能.


|

##### [net.mamoe.mirai.message.data.MessageContent](../net.mamoe.mirai.message.data/-message-content.md)

消息内容


|

##### [net.mamoe.mirai.event.MessageDsl](../net.mamoe.mirai.event/-message-dsl/index.md)

DSL 标记. 将能让 IDE 阻止一些错误的方法调用.


|

##### [net.mamoe.mirai.message.MessageEvent](../net.mamoe.mirai.message/-message-event/index.md)

一个 (收到的) 消息事件.


|

##### [net.mamoe.mirai.message.MessageEventExtensions](../net.mamoe.mirai.message/-message-event-extensions/index.md)

消息事件的扩展函数


|

##### [net.mamoe.mirai.event.MessageListener](../net.mamoe.mirai.event/-message-listener.md)

消息事件的处理器.


|

##### [net.mamoe.mirai.message.data.MessageMetadata](../net.mamoe.mirai.message.data/-message-metadata/index.md)

消息元数据, 即不含内容的元素.


|

##### [net.mamoe.mirai.event.MessagePacketSubscribersBuilder](../net.mamoe.mirai.event/-message-packet-subscribers-builder.md)


|

##### [net.mamoe.mirai.event.events.MessageRecallEvent](../net.mamoe.mirai.event.events/-message-recall-event/index.md)

消息撤回事件. 可是任意消息被任意人撤回.


|

##### [net.mamoe.mirai.message.MessageReceipt](../net.mamoe.mirai.message/-message-receipt/index.md)

发送消息后得到的回执. 可用于撤回, 引用回复等.


|

##### [net.mamoe.mirai.event.MessageSelectBuilder](../net.mamoe.mirai.event/-message-select-builder.md)

[selectMessages](../net.mamoe.mirai.event/select-messages.md) 时的 DSL 构建器.


|

##### [net.mamoe.mirai.event.MessageSelectBuilderUnit](../net.mamoe.mirai.event/-message-select-builder-unit/index.md)

[selectMessagesUnit](../net.mamoe.mirai.event/select-messages-unit.md) 或 [selectMessages](../net.mamoe.mirai.event/select-messages.md) 时的 DSL 构建器.


|

##### [net.mamoe.mirai.event.MessageSelectionTimeoutChecker](../net.mamoe.mirai.event/-message-selection-timeout-checker/index.md)


|

##### [net.mamoe.mirai.event.MessageSelectionTimeoutException](../net.mamoe.mirai.event/-message-selection-timeout-exception/index.md)


|

##### [net.mamoe.mirai.event.events.MessageSendEvent](../net.mamoe.mirai.event.events/-message-send-event/index.md)

主动发送消息


|

##### [net.mamoe.mirai.message.data.MessageSource](../net.mamoe.mirai.message.data/-message-source/index.md)

消息源. 消息源存在于 [MessageChain](../net.mamoe.mirai.message.data/-message-chain/index.md) 中, 用于表示这个消息的来源, 也可以用来分辨 [MessageChain](../net.mamoe.mirai.message.data/-message-chain/index.md).


|

##### [net.mamoe.mirai.message.data.MessageSourceAmender](../net.mamoe.mirai.message.data/-message-source-amender/index.md)

仅于 [copyAmend](../net.mamoe.mirai.message.data/copy-amend.md) 中修改 [MessageSource](../net.mamoe.mirai.message.data/-message-source/index.md)


|

##### [net.mamoe.mirai.message.data.MessageSourceBuilder](../net.mamoe.mirai.message.data/-message-source-builder/index.md)


|

##### [net.mamoe.mirai.event.MessageSubscribersBuilder](../net.mamoe.mirai.event/-message-subscribers-builder/index.md)

消息订阅构造器


|

##### [net.mamoe.mirai.contact.MessageTooLargeException](../net.mamoe.mirai.contact/-message-too-large-exception/index.md)

发送消息时消息过长抛出的异常.


|

##### [net.mamoe.mirai.utils.MiraiExperimentalAPI](../net.mamoe.mirai.utils/-mirai-experimental-a-p-i/index.md)

标记这个类, 类型, 函数, 属性, 字段, 或构造器为实验性的 API.


|

##### [net.mamoe.mirai.utils.MiraiInternalAPI](../net.mamoe.mirai.utils/-mirai-internal-a-p-i/index.md)

标记为一个仅供 Mirai 内部使用的 API.


|

##### [net.mamoe.mirai.utils.MiraiLogger](../net.mamoe.mirai.utils/-mirai-logger/index.md)

日志记录器. 所有的输出均依赖于它.
不同的对象可拥有只属于自己的 logger. 通过 [identity](../net.mamoe.mirai.utils/-mirai-logger/identity.md) 来区分.


|

##### [net.mamoe.mirai.utils.MiraiLoggerPlatformBase](../net.mamoe.mirai.utils/-mirai-logger-platform-base/index.md)

日志基类. 实现了 [follower](../net.mamoe.mirai.utils/-mirai-logger-platform-base/follower.md) 的调用传递.
若 Mirai 自带的日志系统无法满足需求, 请继承这个类或 [PlatformLogger](../net.mamoe.mirai.utils/-platform-logger/index.md) 并实现其抽象函数.


|

##### [net.mamoe.mirai.utils.MiraiLoggerWithSwitch](../net.mamoe.mirai.utils/-mirai-logger-with-switch/index.md)

带有开关的 Logger. 仅能通过 [MiraiLogger.withSwitch](../net.mamoe.mirai.utils/with-switch.md) 构造


|

##### [net.mamoe.mirai.event.events.NewFriendRequestEvent](../net.mamoe.mirai.event.events/-new-friend-request-event/index.md)

一个账号请求添加机器人为好友的事件


|

##### [net.mamoe.mirai.network.NoServerAvailableException](../net.mamoe.mirai.network/-no-server-available-exception/index.md)

无可用服务器


|

##### [net.mamoe.mirai.network.NoStandardInputForCaptchaException](../net.mamoe.mirai.network/-no-standard-input-for-captcha-exception/index.md)

无标准输入或 Kotlin 不支持此输入.


|

##### [net.mamoe.mirai.message.data.OfflineMessageSource](../net.mamoe.mirai.message.data/-offline-message-source/index.md)

由一条消息中的 [QuoteReply](../net.mamoe.mirai.message.data/-quote-reply/index.md) 得到的 [MessageSource](../net.mamoe.mirai.message.data/-message-source/index.md).
此消息源可能来自一条与机器人无关的消息. 因此无法提供对象化的 `sender` 或 `target` 获取.


|

##### [net.mamoe.mirai.message.data.OnlineMessageSource](../net.mamoe.mirai.message.data/-online-message-source/index.md)

在线消息的 [MessageSource](../net.mamoe.mirai.message.data/-message-source/index.md).
拥有对象化的 [sender](../net.mamoe.mirai.message.data/-online-message-source/sender.md), [target](../net.mamoe.mirai.message.data/-online-message-source/target.md), 也可以直接 [recall](../net.mamoe.mirai.message/recall.md) 和 [quote](../net.mamoe.mirai.message/quote.md)


|

##### [net.mamoe.mirai.data.OnlineStatus](../net.mamoe.mirai.data/-online-status/index.md)

在线状态


|

##### [net.mamoe.mirai.message.data.OrNullDelegate](../net.mamoe.mirai.message.data/-or-null-delegate/index.md)

可空的委托


|

##### [net.mamoe.mirai.utils.OverFileSizeMaxException](../net.mamoe.mirai.utils/-over-file-size-max-exception/index.md)

图片文件过大


|

##### [net.mamoe.mirai.contact.PermissionDeniedException](../net.mamoe.mirai.contact/-permission-denied-exception/index.md)

权限不足


|

##### [net.mamoe.mirai.message.data.PlainText](../net.mamoe.mirai.message.data/-plain-text/index.md)

纯文本. 可含 emoji 表情如 😊.


|

##### [net.mamoe.mirai.utils.PlatformLogger](../net.mamoe.mirai.utils/-platform-logger/index.md)

当前平台的默认的日志记录器.
在 *JVM 控制台* 端的实现为 [println](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.io/println.html)
在 *Android* 端的实现为 `android.util.Log`


|

##### [net.mamoe.mirai.message.data.PokeMessage](../net.mamoe.mirai.message.data/-poke-message/index.md)

戳一戳. 可以发送给好友或群.


|

##### [net.mamoe.mirai.message.data.PttMessage](../net.mamoe.mirai.message.data/-ptt-message/index.md)

需要通过上传到服务器的消息，如语音、文件


|

##### [net.mamoe.mirai.message.data.QuoteReply](../net.mamoe.mirai.message.data/-quote-reply/index.md)

引用回复.


|

##### [net.mamoe.mirai.message.data.RichMessage](../net.mamoe.mirai.message.data/-rich-message/index.md)

XML, JSON 消息等富文本消息


| (extensions in package net.mamoe.mirai.message.data)

##### [kotlin.sequences.Sequence](../net.mamoe.mirai.message.data/kotlin.sequences.-sequence/index.md)


|

##### [net.mamoe.mirai.message.data.ServiceMessage](../net.mamoe.mirai.message.data/-service-message/index.md)

服务消息, 可以是 JSON 消息或 XML 消息.


|

##### [net.mamoe.mirai.utils.SilentLogger](../net.mamoe.mirai.utils/-silent-logger/index.md)

不做任何事情的 logger, keep silent.


|

##### [net.mamoe.mirai.event.SimpleListenerHost](../net.mamoe.mirai.event/-simple-listener-host/index.md)

携带一个异常处理器的 [ListenerHost](../net.mamoe.mirai.event/-listener-host.md).


|

##### [net.mamoe.mirai.utils.SimpleLogger](../net.mamoe.mirai.utils/-simple-logger/index.md)

简易日志记录, 所有类型日志都会被重定向 [logger](../net.mamoe.mirai.utils/-simple-logger/logger.md)


|

##### [net.mamoe.mirai.utils.SinceMirai](../net.mamoe.mirai.utils/-since-mirai/index.md)

标记一个自 Mirai 某个版本起才支持或在这个版本修改过的 API.


|

##### [net.mamoe.mirai.utils.SingleFileLogger](../net.mamoe.mirai.utils/-single-file-logger/index.md)

将日志写入('append')到特定文件.


|

##### [net.mamoe.mirai.message.data.SingleMessage](../net.mamoe.mirai.message.data/-single-message.md)

单个消息元素. 与之相对的是 [MessageChain](../net.mamoe.mirai.message.data/-message-chain/index.md), 是多个 [SingleMessage](../net.mamoe.mirai.message.data/-single-message.md) 的集合.


|

##### [net.mamoe.mirai.utils.StandardCharImageLoginSolver](../net.mamoe.mirai.utils/-standard-char-image-login-solver/index.md)

使用字符图片展示验证码, 使用 [input](#) 获取输入, 使用 [overrideLogger](#) 输出


| (extensions in package net.mamoe.mirai.message.data)

##### [kotlin.String](../net.mamoe.mirai.message.data/kotlin.-string/index.md)


|

##### [net.mamoe.mirai.utils.SwingSolver](../net.mamoe.mirai.utils/-swing-solver/index.md)


|

##### [net.mamoe.mirai.utils.SystemDeviceInfo](../net.mamoe.mirai.utils/-system-device-info/index.md)

通过本机信息来获取设备信息.


|

##### [net.mamoe.mirai.message.TempMessageEvent](../net.mamoe.mirai.message/-temp-message-event/index.md)

机器人收到的群临时会话消息的事件


|

##### [net.mamoe.mirai.event.TempMessageSubscribersBuilder](../net.mamoe.mirai.event/-temp-message-subscribers-builder.md)


|

##### [net.mamoe.mirai.utils.Throws](../net.mamoe.mirai.utils/-throws/index.md)

This annotation indicates what exceptions should be declared by a function when compiled to a JVM method.


|

##### [net.mamoe.mirai.utils.UnsafeWeakRef](../net.mamoe.mirai.utils/-unsafe-weak-ref/index.md)

WeakRef that `getValue` for delegation throws an [IllegalStateException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-illegal-state-exception/index.html) if the referent is released by GC. Therefore it returns notnull value only


|

##### [net.mamoe.mirai.network.UnsupportedSMSLoginException](../net.mamoe.mirai.network/-unsupported-s-m-s-login-exception/index.md)

需要短信验证时抛出. mirai 目前还不支持短信验证.


| (extensions in package net.mamoe.mirai.message)

##### [java.net.URL](../net.mamoe.mirai.message/java.net.-u-r-l/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [java.net.URL](../net.mamoe.mirai.utils/java.net.-u-r-l/index.md)


|

##### [net.mamoe.mirai.contact.User](../net.mamoe.mirai.contact/-user/index.md)

代表一个 **用户**.


|

##### [net.mamoe.mirai.message.data.VipFace](../net.mamoe.mirai.message.data/-vip-face/index.md)

VIP 表情.


|

##### [net.mamoe.mirai.message.data.Voice](../net.mamoe.mirai.message.data/-voice/index.md)

语音消息, 目前只支持接收和转发


|

##### [net.mamoe.mirai.utils.WeakRef](../net.mamoe.mirai.utils/-weak-ref/index.md)


| (extensions in package net.mamoe.mirai.utils)

##### [java.lang.ref.WeakReference](../net.mamoe.mirai.utils/java.lang.ref.-weak-reference/index.md)


|

##### [net.mamoe.mirai.utils.WeakRefProperty](../net.mamoe.mirai.utils/-weak-ref-property/index.md)

Indicates that the property is delegated by a [WeakRef](../net.mamoe.mirai.utils/-weak-ref/index.md)


|

##### [net.mamoe.mirai.network.WrongPasswordException](../net.mamoe.mirai.network/-wrong-password-exception/index.md)

密码输入错误 (有时候也会是其他错误, 如 `"当前上网环境异常，请更换网络环境或在常用设备上登录或稍后再试。"`)


|

##### [net.mamoe.mirai.message.data.XmlMessageDsl](../net.mamoe.mirai.message.data/-xml-message-dsl/index.md)


