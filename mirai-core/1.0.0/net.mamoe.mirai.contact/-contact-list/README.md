[mirai-core](../../index.md) / [net.mamoe.mirai.contact](../index.md) / [ContactList](./index.md)

# ContactList

`class ContactList<C : `[`Contact`](../-contact/index.md)`> : `[`Collection`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)`<C>`

只读联系人列表, 无锁链表实现

**See Also**

[ContactList.asSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/as-sequence.html)

### Properties

| Name | Summary |
|---|---|
| [size](size.md) | `val size: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |

### Functions

| Name | Summary |
|---|---|
| [contains](contains.md) | `operator fun contains(element: C): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>`operator fun contains(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [containsAll](contains-all.md) | `fun containsAll(elements: `[`Collection`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)`<C>): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [get](get.md) | `operator fun get(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): C` |
| [getOrNull](get-or-null.md) | `fun getOrNull(id: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`): C?` |
| [isEmpty](is-empty.md) | `fun isEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [iterator](iterator.md) | `fun iterator(): `[`Iterator`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)`<C>` |
| [toString](to-string.md) | `fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Properties

| Name | Summary |
|---|---|
| [idContentString](../id-content-string.md) | ID 列表的字符串表示. 如:`val `[`ContactList`](./index.md)`<*>.idContentString: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
