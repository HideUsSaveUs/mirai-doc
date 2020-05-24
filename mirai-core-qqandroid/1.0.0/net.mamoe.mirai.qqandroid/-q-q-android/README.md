[mirai-core-qqandroid](../../index.md) / [net.mamoe.mirai.qqandroid](../index.md) / [QQAndroid](./index.md)

# QQAndroid

`object QQAndroid : BotFactory`

QQ for Android

### Functions

| Name | Summary |
|---|---|
| [Bot](-bot.md) | 使用指定的 [配置](-bot.md#net.mamoe.mirai.qqandroid.QQAndroid$Bot(net.mamoe.mirai.utils.Context, kotlin.Long, kotlin.String, net.mamoe.mirai.utils.BotConfiguration)/configuration) 构造 [Bot](#) 实例`fun Bot(context: Context, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: BotConfiguration): Bot`<br>`fun Bot(context: Context, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, passwordMd5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, configuration: BotConfiguration): Bot`<br>`fun Bot(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: BotConfiguration = BotConfiguration.Default): Bot`<br>`fun Bot(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, passwordMd5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, configuration: BotConfiguration): Bot` |

### Extension Functions

| Name | Summary |
|---|---|
| [Bot](../-bot.md) | 使用指定的 [配置](../-bot.md#net.mamoe.mirai.qqandroid$Bot(net.mamoe.mirai.qqandroid.QQAndroid, kotlin.Long, kotlin.String, kotlin.Function1((net.mamoe.mirai.utils.BotConfiguration, kotlin.Unit)))/configuration) 构造 [Bot](#) 实例`fun `[`QQAndroid`](./index.md)`.Bot(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: BotConfiguration.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): Bot` |
