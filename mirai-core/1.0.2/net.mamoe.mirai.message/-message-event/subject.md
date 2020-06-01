[mirai-core](../../index.md) / [net.mamoe.mirai.message](../index.md) / [MessageEvent](index.md) / [subject](./subject.md)

# subject

`abstract val subject: `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)

消息事件主体.

* 对于好友消息, 这个属性为 [Friend](../../net.mamoe.mirai.contact/-friend/index.md) 的实例, 与 [sender](sender.md) 引用相同;
* 对于临时会话消息, 这个属性为 [Member](../../net.mamoe.mirai.contact/-member/index.md) 的实例, 与 [sender](sender.md) 引用相同;
* 对于群消息, 这个属性为 [Group](../../net.mamoe.mirai.contact/-group/index.md) 的实例, 与 [GroupMessageEvent.group](../-group-message-event/group.md) 引用相同

在回复消息时, 可通过 [subject](./subject.md) 作为回复对象

