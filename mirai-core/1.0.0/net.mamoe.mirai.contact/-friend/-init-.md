[mirai-core](../../index.md) / [net.mamoe.mirai.contact](../index.md) / [Friend](index.md) / [&lt;init&gt;](./-init-.md)

# &lt;init&gt;

`Friend()`

代表一位好友.

一个 [Friend](index.md) 实例并不是独立的, 它属于一个 [Bot](../../net.mamoe.mirai/-bot/index.md).
对于同一个 [Bot](../../net.mamoe.mirai/-bot/index.md), 任何一个人的 [Friend](index.md) 实例都是单一的.
[Friend](index.md) 无法通过任何方式直接构造. 任何时候都应从 [Bot.getFriend](../../net.mamoe.mirai/-bot/get-friend.md) 或事件中获取.

**See Also**

[FriendMessageEvent](../../net.mamoe.mirai.message/-friend-message-event/index.md)

