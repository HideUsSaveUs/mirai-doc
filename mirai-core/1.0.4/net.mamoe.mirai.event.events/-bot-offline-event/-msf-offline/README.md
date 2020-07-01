[mirai-core](../../../index.md) / [net.mamoe.mirai.event.events](../../index.md) / [BotOfflineEvent](../index.md) / [MsfOffline](./index.md)

# MsfOffline

`@SinceMirai("1.1.0") data class MsfOffline : `[`BotOfflineEvent`](../index.md)`, Packet, `[`BotPassiveEvent`](../../-bot-passive-event.md)`, CauseAware`

被服务器断开

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../../net.mamoe.mirai/-bot/index.md) |
| [cause](cause.md) | `val cause: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?` |
