[mirai-core](../../index.md) / [net.mamoe.mirai.event](../index.md) / [CancellableEvent](./index.md)

# CancellableEvent

`interface CancellableEvent : `[`Event`](../-event/index.md)

可被取消的事件

### Properties

| Name | Summary |
|---|---|
| [isCancelled](is-cancelled.md) | 事件是否已被取消.`abstract val isCancelled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |

### Functions

| Name | Summary |
|---|---|
| [cancel](cancel.md) | 取消这个事件. 事件需实现 [CancellableEvent](./index.md) 接口才可以被取消`abstract fun cancel(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [__broadcastJava](../__broadcast-java.md) | 在 Java 广播一个事件的唯一途径.`fun <E : `[`Event`](../-event/index.md)`> E.__broadcastJava(): E` |
| [broadcast](../broadcast.md) | 广播一个事件的唯一途径.`suspend fun <E : `[`Event`](../-event/index.md)`> E.broadcast(): E` |

### Inheritors

| Name | Summary |
|---|---|
| [BeforeImageUploadEvent](../../net.mamoe.mirai.event.events/-before-image-upload-event/index.md) | 图片上传前. 可以阻止上传.`data class BeforeImageUploadEvent : `[`BotEvent`](../../net.mamoe.mirai.event.events/-bot-event/index.md)`, `[`BotActiveEvent`](../../net.mamoe.mirai.event.events/-bot-active-event.md)`, `[`AbstractEvent`](../-abstract-event/index.md)`, `[`CancellableEvent`](./index.md) |
