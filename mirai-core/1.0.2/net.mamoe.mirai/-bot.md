[mirai-core](../index.md) / [net.mamoe.mirai](index.md) / [Bot](./-bot.md)

# Bot

`inline fun `[`BotFactory`](-bot-factory/index.md)`.Bot(context: `[`Context`](../net.mamoe.mirai.utils/-context/index.md)`, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Bot`](-bot/index.md)
`inline fun `[`BotFactory`](-bot-factory/index.md)`.Bot(context: `[`Context`](../net.mamoe.mirai.utils/-context/index.md)`, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Bot`](-bot/index.md)

使用指定的 [配置](-bot.md#net.mamoe.mirai$Bot(net.mamoe.mirai.BotFactory, net.mamoe.mirai.utils.Context, kotlin.Long, kotlin.String, kotlin.Function1((net.mamoe.mirai.utils.BotConfiguration, kotlin.Unit)))/configuration) 构造 [Bot](-bot/index.md) 实例

`@JvmName("newBot") @JvmOverloads fun Bot(context: `[`Context`](../net.mamoe.mirai.utils/-context/index.md)`, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)` = BotConfiguration.Default): `[`Bot`](-bot/index.md)
`@JvmName("newBot") @JvmOverloads fun Bot(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)` = BotConfiguration.Default): `[`Bot`](-bot/index.md)
`@JvmName("newBot") @JvmOverloads fun Bot(context: `[`Context`](../net.mamoe.mirai.utils/-context/index.md)`, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, passwordMd5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)` = BotConfiguration.Default): `[`Bot`](-bot/index.md)
`@JvmName("newBot") @JvmOverloads fun Bot(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, passwordMd5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)` = BotConfiguration.Default): `[`Bot`](-bot/index.md)

自动加载现有协议的 [BotFactory](-bot-factory/index.md), 并使用指定的 [配置](-bot.md#net.mamoe.mirai$Bot(net.mamoe.mirai.utils.Context, kotlin.Long, kotlin.String, net.mamoe.mirai.utils.BotConfiguration)/configuration) 构造 [Bot](-bot/index.md) 实例

Java 调用方式: `BotFactoryJvm.newBot(...)`

`inline fun Bot(context: `[`Context`](../net.mamoe.mirai.utils/-context/index.md)`, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Bot`](-bot/index.md)
`inline fun Bot(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, password: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Bot`](-bot/index.md)
`inline fun Bot(context: `[`Context`](../net.mamoe.mirai.utils/-context/index.md)`, qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, passwordMd5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Bot`](-bot/index.md)
`inline fun Bot(qq: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, passwordMd5: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, configuration: `[`BotConfiguration`](../net.mamoe.mirai.utils/-bot-configuration/index.md)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Bot`](-bot/index.md)

自动加载现有协议的 [BotFactory](-bot-factory/index.md), 并使用指定的 [配置](-bot.md#net.mamoe.mirai$Bot(net.mamoe.mirai.utils.Context, kotlin.Long, kotlin.String, kotlin.Function1((net.mamoe.mirai.utils.BotConfiguration, kotlin.Unit)))/configuration) 构造 [Bot](-bot/index.md) 实例
