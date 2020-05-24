[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [BotConfiguration](index.md) / [parentCoroutineContext](./parent-coroutine-context.md)

# parentCoroutineContext

`var parentCoroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html)

父 [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html). [Bot](../../net.mamoe.mirai/-bot/index.md) 创建后会使用 [SupervisorJob](#) 覆盖其 [Job](#), 但会将这个 [Job](#) 作为父 [Job](#)

