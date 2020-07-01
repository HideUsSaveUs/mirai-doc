[mirai-core](../../index.md) / [net.mamoe.mirai.message](../index.md) / [GroupMessageEvent](index.md) / [message](./message.md)

# message

`val message: `[`MessageChain`](../../net.mamoe.mirai.message.data/-message-chain/index.md)

消息内容.

第一个元素一定为 [MessageSource](../../net.mamoe.mirai.message.data/-message-source/index.md), 存储此消息的发送人, 发送时间, 收信人, 消息 id 等数据.
随后的元素为拥有顺序的真实消息内容.

