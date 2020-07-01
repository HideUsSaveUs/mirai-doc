[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [BotConfiguration](index.md) / [fileBasedDeviceInfo](./file-based-device-info.md)

# fileBasedDeviceInfo

`@JvmOverloads fun fileBasedDeviceInfo(filepath: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = "device.json"): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

使用文件存储设备信息.

此函数只在 JVM 和 Android 有效. 在其他平台将会抛出异常.

### Parameters

`filepath` - 文件路径. 可相对于程序运行路径 (`user.dir`), 也可以是绝对路径.

**See Also**

[deviceInfo](device-info.md)

