[mirai-core](../../../index.md) / [net.mamoe.mirai.event.events](../../index.md) / [BotOfflineEvent](../index.md) / [Dropped](./index.md)

# Dropped

`data class Dropped : `[`BotOfflineEvent`](../index.md)`, Packet, `[`BotPassiveEvent`](../../-bot-passive-event.md)`, CauseAware`

因网络问题而掉线

### Properties

| Name | Summary |
|---|---|
| [bot](bot.md) | `val bot: `[`Bot`](../../../net.mamoe.mirai/-bot/index.md) |
| [cause](cause.md) | `val cause: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?` |
