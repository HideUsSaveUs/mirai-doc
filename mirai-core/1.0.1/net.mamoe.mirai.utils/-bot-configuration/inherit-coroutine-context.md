[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [BotConfiguration](index.md) / [inheritCoroutineContext](./inherit-coroutine-context.md)

# inheritCoroutineContext

`suspend fun inheritCoroutineContext(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

使用当前协程的 [coroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/coroutine-context.html) 作为 [parentCoroutineContext](parent-coroutine-context.md).

Bot 将会使用一个 [SupervisorJob](#) 覆盖 [coroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/coroutine-context.html) 当前协程的 [Job](#), 并使用当前协程的 [Job](#) 作为父 [Job](#)

用例:

```
coroutineScope {
  val bot = Bot(...) {
    inheritCoroutineContext()
  }
  bot.login()
} // coroutineScope 会等待 Bot 退出
```

**注意**: `bot.cancel` 时将会让父 [Job](#) 也被 cancel.

```
coroutineScope { // this: CoroutineScope
  launch {
    while(isActive) {
      delay(500)
      println("I'm alive")
    }
  }

  val bot = Bot(...) {
     inheritCoroutineContext() // 使用 `coroutineScope` 的 Job 作为父 Job
  }
  bot.login()
  bot.cancel() // 取消了整个 `coroutineScope`, 因此上文不断打印 `"I'm alive"` 的协程也会被取消.
}
```

因此, 此函数尤为适合在 `suspend fun main()` 中使用, 它能阻止主线程退出:

```
suspend fun main() {
  val bot = Bot() {
    inheritCoroutineContext()
  }
  bot.subscribe { ... }

  // 主线程不会退出, 直到 Bot 离线.
}
```

简言之,

* 若想让 [Bot](../../net.mamoe.mirai/-bot/index.md) 作为 '守护进程' 运行, 则无需调用 [inheritCoroutineContext](./inherit-coroutine-context.md).
* 若想让 [Bot](../../net.mamoe.mirai/-bot/index.md) 依赖于当前协程, 让当前协程等待 [Bot](../../net.mamoe.mirai/-bot/index.md) 运行, 则使用 [inheritCoroutineContext](./inherit-coroutine-context.md)

**See Also**

[parentCoroutineContext](parent-coroutine-context.md)

