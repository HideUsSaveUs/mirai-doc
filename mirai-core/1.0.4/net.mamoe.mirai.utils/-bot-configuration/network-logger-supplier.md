[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [BotConfiguration](index.md) / [networkLoggerSupplier](./network-logger-supplier.md)

# networkLoggerSupplier

`var networkLoggerSupplier: (`[`Bot`](../../net.mamoe.mirai/-bot/index.md)`) -> `[`MiraiLogger`](../-mirai-logger/index.md)

网络层日志构造器

* 默认打印到标准输出, 通过 [DefaultLogger](../-default-logger.md)
* 忽略所有日志: [noNetworkLog](no-network-log.md)
* 重定向到一个目录: `networkLoggerSupplier = { DirectoryLogger("Net ${it.id}") }`
* 重定向到一个文件: `networkLoggerSupplier = { SingleFileLogger("Net ${it.id}") }`

**See Also**

[MiraiLogger](../-mirai-logger/index.md)

