[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [java.io.InputStream](./index.md)

### Extensions for java.io.InputStream
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toExternalImage](to-external-image.md) | 将 [InputStream](https://docs.oracle.com/javase/6/docs/api/java/io/InputStream.html) 委托为 [ExternalImage](../-external-image/index.md). 只会在上传图片时才读取 [InputStream](https://docs.oracle.com/javase/6/docs/api/java/io/InputStream.html) 的内容. 具体行为取决于相关 [Bot](../../net.mamoe.mirai/-bot/index.md) 的 [FileCacheStrategy](../-file-cache-strategy/index.md)`fun `[`InputStream`](https://docs.oracle.com/javase/6/docs/api/java/io/InputStream.html)`.toExternalImage(): `[`ExternalImage`](../-external-image/index.md) |

