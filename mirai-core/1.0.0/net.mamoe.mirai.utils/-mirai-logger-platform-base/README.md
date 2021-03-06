[mirai-core](../../index.md) / [net.mamoe.mirai.utils](../index.md) / [MiraiLoggerPlatformBase](./index.md)

# MiraiLoggerPlatformBase

`abstract class MiraiLoggerPlatformBase : `[`MiraiLogger`](../-mirai-logger/index.md)

日志基类. 实现了 [follower](follower.md) 的调用传递.
若 Mirai 自带的日志系统无法满足需求, 请继承这个类或 [PlatformLogger](../-platform-logger/index.md) 并实现其抽象函数.

这个类不应该被用作变量的类型定义. 只应被作为继承对象.
在定义 logger 变量时, 请一直使用 [MiraiLogger](../-mirai-logger/index.md) 或者 [MiraiLoggerWithSwitch](../-mirai-logger-with-switch/index.md).

**See Also**

[PlatformLogger](../-platform-logger/index.md)

[SimpleLogger](../-simple-logger/index.md)

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | 日志基类. 实现了 [follower](follower.md) 的调用传递. 若 Mirai 自带的日志系统无法满足需求, 请继承这个类或 [PlatformLogger](../-platform-logger/index.md) 并实现其抽象函数.`MiraiLoggerPlatformBase()` |

### Properties

| Name | Summary |
|---|---|
| [follower](follower.md) | 随从. 在 this 中调用所有方法后都应继续往 [follower](../-mirai-logger/follower.md) 传递调用. [follower](../-mirai-logger/follower.md) 的存在可以让一次日志被多个日志记录器记录.`var follower: `[`MiraiLogger`](../-mirai-logger/index.md)`?` |
| [isEnabled](is-enabled.md) | 获取 [MiraiLogger](../-mirai-logger/index.md) 是否已开启`open val isEnabled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |

### Functions

| Name | Summary |
|---|---|
| [debug](debug.md) | 记录一个 *调试* 级别的日志.`fun debug(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`fun debug(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [debug0](debug0.md) | `open fun debug0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`abstract fun debug0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [error](error.md) | 记录一个 *错误* 级别的日志.`fun error(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`fun error(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [error0](error0.md) | `open fun error0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`abstract fun error0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [info](info.md) | 记录一个 *信息* 级别的日志.`fun info(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`fun info(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [info0](info0.md) | `open fun info0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`abstract fun info0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [plus](plus.md) | 添加一个 [follower](../-mirai-logger/plus.md#net.mamoe.mirai.utils.MiraiLogger$plus(net.mamoe.mirai.utils.MiraiLogger.plus.T)/follower), 返回 [follower](../-mirai-logger/plus.md#net.mamoe.mirai.utils.MiraiLogger$plus(net.mamoe.mirai.utils.MiraiLogger.plus.T)/follower) 它只会把 `this` 的属性 [MiraiLogger.follower](../-mirai-logger/follower.md) 修改为这个函数的参数 [follower](../-mirai-logger/plus.md#net.mamoe.mirai.utils.MiraiLogger$plus(net.mamoe.mirai.utils.MiraiLogger.plus.T)/follower), 然后返回这个参数. 若 [MiraiLogger.follower](../-mirai-logger/follower.md) 已经有值, 则会替换掉这个值.`open operator fun <T : `[`MiraiLogger`](../-mirai-logger/index.md)`> plus(follower: T): T` |
| [plusAssign](plus-assign.md) | 添加一个 [follower](../-mirai-logger/plus-assign.md#net.mamoe.mirai.utils.MiraiLogger$plusAssign(net.mamoe.mirai.utils.MiraiLogger)/follower) 若 [MiraiLogger.follower](../-mirai-logger/follower.md) 已经有值, 则会对这个值调用 [plusAssign](../-mirai-logger/plus-assign.md). 即会在日志记录器链的末尾添加这个参数 [follower](../-mirai-logger/plus-assign.md#net.mamoe.mirai.utils.MiraiLogger$plusAssign(net.mamoe.mirai.utils.MiraiLogger)/follower)`open fun plusAssign(follower: `[`MiraiLogger`](../-mirai-logger/index.md)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [verbose](verbose.md) | 记录一个 `verbose` 级别的日志. 无关紧要的, 经常大量输出的日志应使用它.`fun verbose(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`fun verbose(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [verbose0](verbose0.md) | `open fun verbose0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`abstract fun verbose0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [warning](warning.md) | 记录一个 *警告* 级别的日志.`fun warning(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`fun warning(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [warning0](warning0.md) | `open fun warning0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`abstract fun warning0(message: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |

### Extension Functions

| Name | Summary |
|---|---|
| [debug](../debug.md) | `fun `[`MiraiLogger`](../-mirai-logger/index.md)`.debug(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`fun `[`MiraiLogger`](../-mirai-logger/index.md)`.debug(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [error](../error.md) | `fun `[`MiraiLogger`](../-mirai-logger/index.md)`.error(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`fun `[`MiraiLogger`](../-mirai-logger/index.md)`.error(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [info](../info.md) | `fun `[`MiraiLogger`](../-mirai-logger/index.md)`.info(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`fun `[`MiraiLogger`](../-mirai-logger/index.md)`.info(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [verbose](../verbose.md) | `fun `[`MiraiLogger`](../-mirai-logger/index.md)`.verbose(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`fun `[`MiraiLogger`](../-mirai-logger/index.md)`.verbose(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [warning](../warning.md) | `fun `[`MiraiLogger`](../-mirai-logger/index.md)`.warning(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>`fun `[`MiraiLogger`](../-mirai-logger/index.md)`.warning(lazyMessage: () -> `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, e: `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`?): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [withSwitch](../with-switch.md) | 给这个 logger 添加一个开关, 用于控制是否记录 log`fun `[`MiraiLogger`](../-mirai-logger/index.md)`.withSwitch(default: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = true): `[`MiraiLoggerWithSwitch`](../-mirai-logger-with-switch/index.md) |

### Inheritors

| Name | Summary |
|---|---|
| [MiraiLoggerWithSwitch](../-mirai-logger-with-switch/index.md) | 带有开关的 Logger. 仅能通过 [MiraiLogger.withSwitch](../with-switch.md) 构造`class MiraiLoggerWithSwitch : `[`MiraiLoggerPlatformBase`](./index.md) |
| [PlatformLogger](../-platform-logger/index.md) | 当前平台的默认的日志记录器. 在 *JVM 控制台* 端的实现为 [println](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.io/println.html) 在 *Android* 端的实现为 `android.util.Log``open class PlatformLogger : `[`MiraiLoggerPlatformBase`](./index.md) |
| [SimpleLogger](../-simple-logger/index.md) | 简易日志记录, 所有类型日志都会被重定向 [logger](../-simple-logger/logger.md)`open class SimpleLogger : `[`MiraiLoggerPlatformBase`](./index.md) |
