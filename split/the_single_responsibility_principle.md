---
aliases:
- 单一功能原则
- 单一职责原则
- The Single Responsibility Principle
- SRP
category:
- 方法论
- hacker-law
name: The Single Responsibility Principle
tag:
- 单一功能原则
- 单一功能
zhname: 单一功能原则
id: 20220703231618_01d9dd1c22394e1a
---

# 单一功能原则 (The Single Responsibility Principle)

- [英文维基百科](https://en.wikipedia.org/wiki/Single_responsibility_principle)
- [中文维基百科](https://zh.wikipedia.org/wiki/%E5%8D%95%E4%B8%80%E5%8A%9F%E8%83%BD%E5%8E%9F%E5%88%99)

> 每个模块或者类只应该有一项功能。

[[SOLID]] 的第一个原则。这个原则表明模块或者类只应该做一件事。实际上，这意味着对程序功能的单个小更改，应该只需要更改一个组件。例如，更改密码验证复杂性的方式应该只需要更改程序的一部分。

理论上讲，这使代码更健壮，更容易更改。知道正在更改的组件只有一个功能，这意味着测试更改更容易。使用前面的例子，更改密码复杂性组件应该只影响与密码复杂性相关的功能。变更具有许多功能的组件可能要困难得多。

## [[架构的整洁之道]] 中的表述

最初的表述: **任何一个软件模块都应该有且仅有一个*被修改的原因***.

"被修改的原因"可以这样理解并修改表述:
**任何一个软件模块都应该只对应一个用户(User)或系统利益相关者(Stakeholder)负责**.

在这里我们对"用户"和"利益相关者"的形容并不准确, 它们可能指的是一个或多个利益相关者, 只要这些人希望对系统进行变更是相似的, 就可以归为一类. 在这里, 我们将其称为"行为者(actor)"

最终的描述: **任何一个软件模块都应该只对一类行为者负责**.

单一职责主要讨论的是函数和类之间的关系. 但在不同的层面上也会有着不同的名字, 在组件层面上称为"共同闭包原则(Common Closure Principle)"; 在软件架构层面上, 则是用于奠定**架构边界**的"变更轴心(Axis of Change)"

## 参考
- [Object-Orientated Programming](#todo)
- [[solid|SOLID]]

## 如何践行

* 可以轻松的起一个合适的名字
* 可以用一句话进行准确的行为描述清楚