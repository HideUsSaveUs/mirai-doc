[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [java.net.URL](index.md) / [toExternalImage](./to-external-image.md)

# toExternalImage

`fun `[`URL`](https://docs.oracle.com/javase/6/docs/api/java/net/URL.html)`.toExternalImage(): `[`ExternalImage`](../-external-image/index.md)

将 [URL](https://docs.oracle.com/javase/6/docs/api/java/net/URL.html) 委托为 [ExternalImage](../-external-image/index.md).
只会在上传图片时才读取 [URL](https://docs.oracle.com/javase/6/docs/api/java/net/URL.html) 的内容. 具体行为取决于相关 [Bot](../../net.mamoe.mirai/-bot/index.md) 的 [FileCacheStrategy](../-file-cache-strategy/index.md)

