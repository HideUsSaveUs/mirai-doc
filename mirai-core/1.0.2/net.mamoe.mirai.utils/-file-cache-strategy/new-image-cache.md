[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [FileCacheStrategy](index.md) / [newImageCache](./new-image-cache.md)

# newImageCache

`abstract fun newImageCache(input: Input): `[`ExternalImage`](../-external-image/index.md)

将 [input](new-image-cache.md#net.mamoe.mirai.utils.FileCacheStrategy$newImageCache(kotlinx.io.core.Input)/input) 缓存为 [ExternalImage](../-external-image/index.md).
此函数应 close 这个 [Input](#)

`abstract fun newImageCache(input: InputStream): `[`ExternalImage`](../-external-image/index.md)

将 [input](new-image-cache.md#net.mamoe.mirai.utils.FileCacheStrategy$newImageCache(java.io.InputStream)/input) 缓存为 [ExternalImage](../-external-image/index.md).
此函数应 close 这个 [InputStream](https://docs.oracle.com/javase/6/docs/api/java/io/InputStream.html)

`abstract fun newImageCache(input: `[`ByteArray`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`): `[`ExternalImage`](../-external-image/index.md)
`abstract fun newImageCache(input: `[`BufferedImage`](https://docs.oracle.com/javase/6/docs/api/java/awt/image/BufferedImage.html)`, format: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = "png"): `[`ExternalImage`](../-external-image/index.md)

将 [input](new-image-cache.md#net.mamoe.mirai.utils.FileCacheStrategy$newImageCache(kotlin.ByteArray)/input) 缓存为 [ExternalImage](../-external-image/index.md).
此 [input](new-image-cache.md#net.mamoe.mirai.utils.FileCacheStrategy$newImageCache(kotlin.ByteArray)/input) 的内容应是不变的.

`abstract fun newImageCache(input: `[`URL`](https://docs.oracle.com/javase/6/docs/api/java/net/URL.html)`): `[`ExternalImage`](../-external-image/index.md)

将 [input](new-image-cache.md#net.mamoe.mirai.utils.FileCacheStrategy$newImageCache(java.net.URL)/input) 缓存为 [ExternalImage](../-external-image/index.md).

