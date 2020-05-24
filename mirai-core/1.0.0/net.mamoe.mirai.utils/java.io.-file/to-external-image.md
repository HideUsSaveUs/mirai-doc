[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [java.io.File](index.md) / [toExternalImage](./to-external-image.md)

# toExternalImage

`@JvmOverloads fun `[`File`](https://docs.oracle.com/javase/6/docs/api/java/io/File.html)`.toExternalImage(deleteOnClose: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`ExternalImage`](../-external-image/index.md)

将文件作为 [ExternalImage](../-external-image/index.md) 使用. 只会在需要的时候打开文件并读取数据.

### Parameters

`deleteOnClose` - 若为 `true`, 图片发送后将会删除这个文件