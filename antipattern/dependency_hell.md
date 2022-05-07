---
aliases:
- "Dependency hell"
- "依赖地狱"
- "相依性地狱"
name: "Dependency hell"
zhname: "依赖地狱"
zhwiki: "https://zh.wikipedia.org/wiki/%E4%BE%9D%E8%B5%96%E5%9C%B0%E7%8B%B1"
groups: "配置管理"
category:
- 反面模式
- antipattern
- 方法论
---

# 依赖地狱

* [wiki:依赖地狱](https://zh.wikipedia.org/wiki/%E4%BE%9D%E8%B5%96%E5%9C%B0%E7%8B%B1)

所依赖产品的版本所导致的问题

相依性地狱（英语：dependency hell），又称依赖地狱，是指在操作系统中由于软件之间的依赖性不能被满足而引发的问题。

一个软件包依赖于其它必要的软件包（且版本要符合要求），使得软件包系统形成了复杂的依赖关系网络，并可能引发一系列问题。一些软件包可能因为依赖性无法满足，需要安装大量软件包；另一方面，一个软件包的卸载可能引发数量众多的软件包无法工作。