[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [java.io.File](./index.md)

### Extensions for java.io.File

"
                                    |||
                                    |:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
                                    | [loadAsDeviceInfo](load-as-device-info.md) | 加载一个设备信息. 若文件不存在或为空则随机并创建一个设备信息保存.`fun `[`File`](https://docs.oracle.com/javase/6/docs/api/java/io/File.html)`.loadAsDeviceInfo(context: `[`Context`](../-context/index.md)` = ContextImpl()): `[`DeviceInfo`](../-device-info/index.md) |
| [toExternalImage](to-external-image.md) | 将文件作为 [ExternalImage](../-external-image/index.md) 使用. 只会在需要的时候打开文件并读取数据.`fun `[`File`](https://docs.oracle.com/javase/6/docs/api/java/io/File.html)`.toExternalImage(deleteOnClose: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`ExternalImage`](../-external-image/index.md) |

