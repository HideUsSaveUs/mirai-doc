[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [PlatformLogger](index.md) / [&lt;init&gt;](./-init-.md)

# &lt;init&gt;

`PlatformLogger(identity: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`? = "Mirai")`

当前平台的默认的日志记录器.
在 *JVM 控制台* 端的实现为 [println](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.io/println.html)
在 *Android* 端的实现为 `android.util.Log`

单条日志格式 (正则) 为:

``` regex
^([\w-]*\s[\w:]*)\s(\w)\/(.*?):\s(.+)$
```

其中 group 分别为: 日期与时间, 严重程度, [identity](#), 消息内容.

示例:

``` log
2020-05-21 19:51:09 V/Bot 1994701021: Send: OidbSvc.0x88d_7
```

日期时间格式为 `yyyy-MM-dd HH:mm:ss`,

严重程度为 V, I, W, E. 分别对应 verbose, info, warning, error

**See Also**

[DefaultLogger](../-default-logger.md)

`PlatformLogger(identity: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`? = "Mirai", output: (`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`, isColored: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true)`

JVM 控制台日志实现

单条日志格式 (正则) 为:

``` regex
^([\w-]*\s[\w:]*)\s(\w)\/(.*?):\s(.+)$
```

其中 group 分别为: 日期与时间, 严重程度, [identity](identity.md), 消息内容.

示例:

``` log
2020-05-21 19:51:09 V/Bot 1994701021: Send: OidbSvc.0x88d_7
```

日期时间格式为 `yyyy-MM-dd HH:mm:ss`,

严重程度为 V, I, W, E. 分别对应 verbose, info, warning, error

### Parameters

`isColored` - 是否添加 ANSI 颜色

**See Also**

[DefaultLogger](../-default-logger.md)

[SingleFileLogger](../-single-file-logger/index.md)

[DirectoryLogger](../-directory-logger/index.md)

