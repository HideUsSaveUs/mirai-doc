[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [BotConfiguration](./index.md)

# BotConfiguration

`open class BotConfiguration`

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

### Types

| Name | Summary |
|---|---|
| [MiraiProtocol](-mirai-protocol/index.md) | `enum class MiraiProtocol` |

### Annotations

| Name | Summary |
|---|---|
| [ConfigurationDsl](-configuration-dsl/index.md) | 标注一个配置 DSL 函数`annotation class ConfigurationDsl` |

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | [Bot](../../net.mamoe.mirai/-bot/index.md) 配置.`BotConfiguration()` |

### Properties

| Name | Summary |
|---|---|
| [botLoggerSupplier](bot-logger-supplier.md) | 日志记录器`var botLoggerSupplier: (`[`Bot`](../../net.mamoe.mirai/-bot/index.md)`) -> `[`MiraiLogger`](../-mirai-logger/index.md) |
| [deviceInfo](device-info.md) | 设备信息覆盖. 在没有手动指定时将会通过日志警告, 并使用随机设备信息.`var deviceInfo: ((`[`Context`](../-context/index.md)`) -> `[`DeviceInfo`](../-device-info/index.md)`)?` |
| [fileCacheStrategy](file-cache-strategy.md) | 缓存策略`var fileCacheStrategy: `[`FileCacheStrategy`](../-file-cache-strategy/index.md) |
| [firstReconnectDelayMillis](first-reconnect-delay-millis.md) | 心跳失败后的第一次重连前的等待时间.`var firstReconnectDelayMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [heartbeatPeriodMillis](heartbeat-period-millis.md) | 心跳周期. 过长会导致被服务器断开连接.`var heartbeatPeriodMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [heartbeatTimeoutMillis](heartbeat-timeout-millis.md) | 每次心跳时等待结果的时间. 一旦心跳超时, 整个网络服务将会重启 (将消耗约 1s). 除正在进行的任务 (如图片上传) 会被中断外, 事件和插件均不受影响.`var heartbeatTimeoutMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [loginSolver](login-solver.md) | 验证码处理器`var loginSolver: `[`LoginSolver`](../-login-solver/index.md) |
| [networkLoggerSupplier](network-logger-supplier.md) | 网络层日志构造器`var networkLoggerSupplier: (`[`Bot`](../../net.mamoe.mirai/-bot/index.md)`) -> `[`MiraiLogger`](../-mirai-logger/index.md) |
| [parentCoroutineContext](parent-coroutine-context.md) | 父 [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html). [Bot](../../net.mamoe.mirai/-bot/index.md) 创建后会使用 [SupervisorJob](#) 覆盖其 [Job](#), 但会将这个 [Job](#) 作为父 [Job](#)`var parentCoroutineContext: `[`CoroutineContext`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) |
| [protocol](protocol.md) | 使用协议类型`var protocol: MiraiProtocol` |
| [reconnectionRetryTimes](reconnection-retry-times.md) | 最多尝试多少次重连`var reconnectionRetryTimes: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [reconnectPeriodMillis](reconnect-period-millis.md) | 重连失败后, 继续尝试的每次等待时间`var reconnectPeriodMillis: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |

### Functions

| Name | Summary |
|---|---|
| [copy](copy.md) | `fun copy(): `[`BotConfiguration`](./index.md) |
| [fileBasedDeviceInfo](file-based-device-info.md) | 使用文件存储设备信息.`fun fileBasedDeviceInfo(filepath: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = "device.json"): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [inheritCoroutineContext](inherit-coroutine-context.md) | 使用当前协程的 [coroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/coroutine-context.html) 作为 [parentCoroutineContext](parent-coroutine-context.md).`suspend fun inheritCoroutineContext(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [noBotLog](no-bot-log.md) | 不显示 [Bot](../../net.mamoe.mirai/-bot/index.md) 日志. 不推荐.`fun noBotLog(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [noNetworkLog](no-network-log.md) | 不显示网络日志. 不推荐.`fun noNetworkLog(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [randomDeviceInfo](random-device-info.md) | 使用随机设备信息.`fun randomDeviceInfo(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |

### Companion Object Properties

| Name | Summary |
|---|---|
| [Default](-default.md) | 默认的配置实例. 可以进行修改`val Default: `[`BotConfiguration`](./index.md) |
