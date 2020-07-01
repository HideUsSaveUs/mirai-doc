[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [ServiceMessage](index.md) / [&lt;init&gt;](./-init-.md)

# &lt;init&gt;

`ServiceMessage(serviceId: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)`

服务消息, 可以是 JSON 消息或 XML 消息.

JSON 消息更多情况下通过 [LightApp](../-light-app/index.md) 发送.

### Parameters

`serviceId` - 目前未知, XML 一般为 60, JSON 一般为 1

`content` - 消息内容. 可为 JSON 文本或 XML 文本

**See Also**

[LightApp](../-light-app/index.md)

