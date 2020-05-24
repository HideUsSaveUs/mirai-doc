[mirai-core](../index.md) / [net.mamoe.mirai.event](index.md) / [MessageSelectBuilder](./-message-select-builder.md)

# MessageSelectBuilder

`abstract class MessageSelectBuilder<M : `[`MessageEvent`](../net.mamoe.mirai.message/-message-event/index.md)`, R> : `[`MessageSelectBuilderUnit`](-message-select-builder-unit/index.md)`<M, R>`

[selectMessages](select-messages.md) 时的 DSL 构建器.

它是特殊化的消息监听 ([CoroutineScope.subscribeMessages](#)) DSL, 屏蔽了一些 `reply` DSL 以确保作用域安全性

**See Also**

[MessageSelectBuilderUnit](-message-select-builder-unit/index.md)

