[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [BotConfiguration](index.md) / [&lt;init&gt;](./-init-.md)

# &lt;init&gt;

`BotConfiguration()`

[Bot](../../net.mamoe.mirai/-bot/index.md) 配置.

Kotlin 使用方法:

```
val bot = Bot(...) {
   // 在这里配置 Bot

   bogLoggerSupplier = { bot -> ... }
   fileBasedDeviceInfo()
   inheritCoroutineContext() // 使用 `coroutineScope` 的 Job 作为父 Job
}
```

