[mirai-core](../../index.md) / [net.mamoe.mirai.message.data](../index.md) / [ForwardMessage](./index.md)

# ForwardMessage

`class ForwardMessage : `[`MessageContent`](../-message-content.md)

合并转发消息

### 显示方案

#### 移动端

在移动客户端将会显示为卡片

`<title>`: [DisplayStrategy.generateTitle](-display-strategy/generate-title.md)

`<preview>`: [DisplayStrategy.generatePreview](-display-strategy/generate-preview.md)

`<summary>`: [DisplayStrategy.generateSummary](-display-strategy/generate-summary.md)

```
|-------------------------|
| <title>                 |
| <preview>               |
|-------------------------|
| <summary>               |
|-------------------------|
```

默认显示方案:

```
|-------------------------|
| 群聊的聊天记录             |
| <消息 1>                 |
| <消息 2>                 |
| <消息 3>                 |
|-------------------------|
| 查看 3 条转发消息          |
|-------------------------|
```

#### PC 端

在部分 PC 端显示为类似移动端的卡片, 在其他 PC 端显示为以下格式

```
鸽子 A 2020/04/23 11:27:54
咕
鸽子 B 2020/04/23 11:27:55
咕
鸽子 C 1970/01/01 08:00:00
咕咕咕
```

### 构造

* 使用 [DSL](../build-forward-message.md)
* 通过 [MessageEvent](../../net.mamoe.mirai.message/-message-event/index.md) 集合转换: [toForwardMessage](../kotlin.collections.-iterable/to-forward-message.md)

### Parameters

`displayStrategy` - 卡片显示方案

**See Also**

[buildForwardMessage](../build-forward-message.md)

### Types

| Name | Summary |
|---|---|
| [DisplayStrategy](-display-strategy/index.md) | `abstract class DisplayStrategy` |
| [INode](-i-node/index.md) | `interface INode` |
| [Key](-key/index.md) | `companion object Key : Key<`[`ForwardMessage`](./index.md)`>` |
| [Node](-node/index.md) | `data class Node : INode` |

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | 合并转发消息`ForwardMessage(nodeList: `[`Collection`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)`<INode>, displayStrategy: DisplayStrategy = DisplayStrategy.Default)` |

### Properties

| Name | Summary |
|---|---|
| [displayStrategy](display-strategy.md) | 卡片显示方案`val displayStrategy: DisplayStrategy` |
| [nodeList](node-list.md) | 消息列表`val nodeList: `[`Collection`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)`<INode>` |

### Functions

| Name | Summary |
|---|---|
| [contentToString](content-to-string.md) | 转为最接近官方格式的字符串. 如 `At(member) + "test"` 将转为 `"@群名片 test"`.`fun contentToString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [toString](to-string.md) | 得到包含 mirai 消息元素代码的, 易读的字符串. 如 `At(member) + "test"` 将转为 `"[mirai:at:qqId]test"``fun toString(): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Companion Object Properties

| Name | Summary |
|---|---|
| [typeName](type-name.md) | 此 [Key](../-message/-key/index.md) 指代的 [Message](../-message/index.md) 类型名. 一般为 `class.simpleName`, 如 "QuoteReply", "PlainText"`val typeName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Properties

| Name | Summary |
|---|---|
| [content](../content.md) | [Message.contentToString](../-message/content-to-string.md) 的捷径`val `[`Message`](../-message/index.md)`.content: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [flatten](../flatten.md) | 扁平化 [Message](../-message/index.md)`fun `[`Message`](../-message/index.md)`.flatten(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`SingleMessage`](../-single-message.md)`>` |
| [isContentEmpty](../is-content-empty.md) | 判断消息内容是否为空.`fun `[`Message`](../-message/index.md)`.isContentEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isContentNotEmpty](../is-content-not-empty.md) | `fun `[`Message`](../-message/index.md)`.isContentNotEmpty(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isNotPlain](../is-not-plain.md) | `fun `[`Message`](../-message/index.md)`.isNotPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isPlain](../is-plain.md) | `fun `[`Message`](../-message/index.md)`.isPlain(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [plus](../plus.md) | `suspend operator fun `[`Message`](../-message/index.md)`.plus(another: Flow<`[`Message`](../-message/index.md)`>): `[`MessageChain`](../-message-chain/index.md) |
| [repeat](../repeat.md) | 将此消息元素按顺序重复 [count](../repeat.md#net.mamoe.mirai.message.data$repeat(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`fun `[`Message`](../-message/index.md)`.repeat(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) |
| [sendTo](../send-to.md) | `suspend fun <C : `[`Contact`](../../net.mamoe.mirai.contact/-contact/index.md)`> `[`Message`](../-message/index.md)`.sendTo(contact: C): `[`MessageReceipt`](../../net.mamoe.mirai.message/-message-receipt/index.md)`<C>` |
| [times](../times.md) | 将此消息元素按顺序重复 [count](../times.md#net.mamoe.mirai.message.data$times(net.mamoe.mirai.message.data.Message, kotlin.Int)/count) 次.`operator fun `[`Message`](../-message/index.md)`.times(count: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`): `[`MessageChain`](../-message-chain/index.md) |
| [toForwardMessage](../to-forward-message.md) | 转换为 [ForwardMessage](./index.md)`fun `[`Message`](../-message/index.md)`.toForwardMessage(sender: `[`User`](../../net.mamoe.mirai.contact/-user/index.md)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](./index.md)<br>`fun `[`Message`](../-message/index.md)`.toForwardMessage(senderId: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, senderName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, time: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` = currentTimeSeconds.toInt(), displayStrategy: DisplayStrategy = DisplayStrategy): `[`ForwardMessage`](./index.md) |
