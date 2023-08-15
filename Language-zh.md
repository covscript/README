# CovScript 的语言设计
## 发展历史
CovScript 最初发布于 2017 年，其前身是一种类 Basic 语言 CovBasic，这为 CovScript 的语言设计打下了重要的基础。
除此之外，CovScript 的设计还参考了 Lua、C++、Java 等一系列现代语言。
目前 CovScript 解释器已发展至第三代（CovScript 3，简称 Cov3 或 Legacy CovScript）。

从 2020 年开始，CovScript 4（简称 Cov4 或 ECS, *Extended CovScript*）开始设计。
但由于一系列变故导致设计一拖再拖，直到 2022 年重启设计工作，于 2023 年正式并入主线。
## 设计模式
CovScript 的设计不是理论主导的，更多是工程经验主导，其诞生目的也不是想创造一个在理论上比较完美的语言。
CovScript 最初是想打造一个类 C 编程思想、语法比较简单的动态类型语言，因此有了以下的特性：
 + 仅有基础的控制语句，如 if、while、loop、for、foreach、switch 等
 + 仅有基础的面向对象：仅支持单继承，不支持任何形式的访问保护（Private、Public 等）

但 CovScript 也提供了一些较为灵活、易用的现代语言基础设施：
 + 动态强类型，即类型是动态变化的，但不能进行任何形式的隐式转换
 + 函数即对象，也支持 Lambda 表达式方便实现闭包

资源管理方面，CovScript 融合了基于范围的变量生命周期（类似 C++ 的 RAII）和 GC：
 + CovScript 在语言层面上是保证了资源安全的，用户大多数时候无需担心资源管理的问题
 + 但由于类 RAII 机制的存在，再加上变量的类型是动态的，GC 在大多数情况下不是必须的
 + 具体可参考 [CovScript 变量的生命周期](https://csman.info/doku.php?id=manual:reference:grammar:type_system:main_page#变量的生命周期)

语言特性方面，CovScript 采取语言核心提供基础设施、外围库提供扩展语义的方式，减少语言核心标准的频繁变动带来的负面影响。
 + 比如协程（Coroutine），语言核心仅提供了较为原始的 API，抽象程度较高的 Coroutine Scheduler 则在 Standard Utilities 中提供
 + 简单的总结，就是**能用库实现的就不动语言标准**

在语言生态上，CovScript 目前采取的策略如下：
 + 坚持以自建生态为主，C/C++ 生态为辅，对其他语言的相互兼容和互操作持开放态度
 + CovScript 3 的标准将谨慎修订，未来逐渐发展成基座语言，为包括 CovScript 4 在内的子语言提供基础设施
