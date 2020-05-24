[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [UnsafeWeakRef](./index.md)

# UnsafeWeakRef

`class UnsafeWeakRef<T>`

WeakRef that `getValue` for delegation throws an [IllegalStateException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-illegal-state-exception/index.html) if the referent is released by GC. Therefore it returns notnull value only

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | WeakRef that `getValue` for delegation throws an [IllegalStateException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-illegal-state-exception/index.html) if the referent is released by GC. Therefore it returns notnull value only`UnsafeWeakRef(weakRef: `[`WeakRef`](../-weak-ref/index.md)`<T>)` |

### Functions

| Name | Summary |
|---|---|
| [clear](clear.md) | `fun clear(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [get](get.md) | `fun get(): T` |

### Extension Functions

| Name | Summary |
|---|---|
| [getValue](../get-value.md) | Provides delegate value.`operator fun <T> `[`UnsafeWeakRef`](./index.md)`<T>.getValue(thisRef: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`?, property: `[`KProperty`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-property/index.html)`<*>): T` |
