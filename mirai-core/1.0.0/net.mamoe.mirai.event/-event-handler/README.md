[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [EventHandler](./index.md)

# EventHandler

`@Target([AnnotationTarget.FUNCTION]) annotation class EventHandler`

标注一个函数为事件监听器.

### Kotlin 函数

Kotlin 函数要求:

* 接收者 (英 receiver) 和函数参数: 所标注的 Kotlin 函数必须至少拥有一个接收者或一个函数参数, 或二者都具有. 接收者和函数参数的类型必须相同 (如果二者都存在)
接收者或函数参数的类型都必须为 [Event](../-event/index.md) 或其子类.
* 返回值: 为 [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) 或不指定返回值时将注册为 [CoroutineScope.subscribeAlways](../kotlinx.coroutines.-coroutine-scope/subscribe-always.md), 为 [ListeningStatus](../-listening-status/index.md) 时将注册为 [CoroutineScope.subscribe](../kotlinx.coroutines.-coroutine-scope/subscribe.md).
任何其他类型的返回值将会在注册时抛出异常.

所有 Kotlin 非 `suspend` 的函数都将会在 [Dispatchers.IO](#) 中调用

支持的函数类型:

```
suspend fun T.onEvent(T)
suspend fun T.onEvent(T): ListeningStatus
suspend fun onEvent(T)
suspend fun onEvent(T): ListeningStatus
suspend fun T.onEvent()
suspend fun T.onEvent(): ListeningStatus
fun T.onEvent(T)
fun T.onEvent(T): ListeningStatus
fun onEvent(T)
fun onEvent(T): ListeningStatus
fun T.onEvent()
fun T.onEvent(): ListeningStatus
```

Kotlin 使用示例:

* 独立 [CoroutineScope](#) 和 [ListenerHost](../-listener-host.md)

```
object MyEvents : ListenerHost {
    override val coroutineContext = SupervisorJob()

    @EventHandler
    suspend fun MessageEvent.onMessage() {
        reply("received")
    }
}

myCoroutineScope.registerEvents(MyEvents)
```

`onMessage` 抛出的异常将会交给 `myCoroutineScope` 处理

* 合并 [CoroutineScope](#) 和 [ListenerHost](../-listener-host.md): 使用 [SimpleListenerHost](../-simple-listener-host/index.md)

```
object MyEvents : SimpleListenerHost( /* override coroutineContext here */) {
    override fun handleException(context: CoroutineContext, exception: Throwable) {
        // 处理 onMessage 中未捕获的异常
    }

    @EventHandler
    suspend fun MessageEvent.onMessage() {
        reply("received")
    }
}

MyEvents.registerEvents()
```

### Java 方法

所有 Java 方法都会在 [Dispatchers.IO](#) 中调用.

支持的方法类型

```
void onEvent(T)
ListeningStatus onEvent(T)
```

Java 使用示例:

```
public class MyEventHandlers extends SimpleListenerHost {
    @Override
    public void handleException(CoroutineContext context, Throwable exception){
        // 处理事件处理时抛出的异常
    }

    @EventHandler
    public void onMessage(MessageEvent event) throws Exception {
        event.subject.sendMessage("received")
    }
}

Events.registerEvents(new MyEventHandlers())
```

``` kotlin
//Unresolved: net.mamoe.mirai.event.JvmMethodEventsTest
```

### Constructors
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [&lt;init&gt;](-init-.md) | 标注一个函数为事件监听器.`EventHandler(priority: EventPriority = EventPriority.NORMAL, ignoreCancelled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true, concurrency: ConcurrencyKind = Listener.ConcurrencyKind.CONCURRENT)` |

### Properties
|||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [concurrency](concurrency.md) | 并发类型`val concurrency: ConcurrencyKind` ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ignoreCancelled](ignore-cancelled.md) | 是否自动忽略被 [取消](../-cancellable-event/is-cancelled.md)`val ignoreCancelled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) ||||
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [priority](priority.md) | 监听器优先级`val priority: EventPriority` |

