---
aliases:
- Database-as-IPC
- 数据库式进程间通信
name: Database-as-IPC
zhname: 数据库式进程间通信
wiki: https://en.wikipedia.org/wiki/Database-as-IPC
groups: 软件设计
category:
- 反面模式
- antipattern
- 方法论
id: 20220703224535_ad318a472cdf4980
---

# 数据库式进程间通信

* [wiki:https://en.wikipedia.org/wiki/Database-as-IPC](https://en.wikipedia.org/wiki/Database-as-IPC)

使用数据库进行[进程间通信](https://zh.wikipedia.org/wiki/%E8%BF%9B%E7%A8%8B%E9%97%B4%E9%80%9A%E4%BF%A1)，而不使用更轻量级的合适的机制。或者说，对于常规的[进程间通信](https://zh.wikipedia.org/wiki/%E8%BF%9B%E7%A8%8B%E9%97%B4%E9%80%9A%E4%BF%A1)，不是去采用轻量得多的合适机制，而是将数据库用作消息队列。
