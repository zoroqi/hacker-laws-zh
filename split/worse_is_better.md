---
id: 20230506144505_0cb9bd560804499e
date: "2023-05-06"
aliases:
- Worse Is Better
- 越糟糕越好
category:
- 方法论
- hacker-law
name: Worse Is Better
tags:
- 程序理论
zhname: 越糟糕越好
---

原文: [The Rise of Worse is Better](https://dreamsongs.com/WIB.html) [archive](https://web.archive.org/web/20230412073703/https://dreamsongs.com/WIB.html)

[Lisp: Good News, Bad News, How to Win Big](https://www.dreamsongs.com/WIB.html) [archive](https://web.archive.org/web/20230412073703/https://dreamsongs.com/WIB.html) 

Worse is Better，强调**简单压倒一切**，为了简单性，其他方便都可以做出牺牲，包含以下几点

1. 简单性：设计必须简单，这既是对实现的要求，也是对接口的要求。实现的简单要比接口的简单更加重要。简单是设计中需要第一重视的因素。
2. 正确性：设计在任何值得注意的方面都要求正确。为了简单性，正确性可以做轻微的让步。
3. 一致性：设计不能过度不兼容一致。为了简单，一致性可以在某些方面做些牺牲，但与其允许设计中的这些处理不常见情况的部分去增加实现的复杂性和不一致性，不如丢掉它们。
4. 完整性：设计必须覆盖到实际应用的各种重要场景。所有可预料到的情况都应该覆盖到。为了保证其它几种特征的品质，完整性可以作出牺牲。事实上，一旦简单性受到危害，完整性必须做出牺牲。一致性可以为实现的完整性作出牺牲；最不重要的是接口上的一致性。

从这件事中我们学到的是,一开始就来做正确的事是不可取的.更好的做法是先完成正确的事的一半,可以使得传播的速度像病毒一样.一旦人们迷上了它,再花时间做到正确的事的90%.

> [!NOTE]
> 可以理解成一种"小步快跑"的理念

* [[2023-06-12-11#2.1 The Rise of Worse is Better]]
* [[all_models_are_wrong_or_george_boxs_law|乔治·伯克斯定律]]
* [[hutbers_law|哈特伯定律]]
* [[galls_law|盖尔定律]]