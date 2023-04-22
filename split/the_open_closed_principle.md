---
aliases:
- 开闭原则
- The Open/Closed Principle
- OCP
category:
- 方法论
- hacker-law
name: The Open/Closed Principle
tag:
- 开闭原则
- 开闭
zhname: 开闭原则
id: 20220703234010_05ef000bd1de45a6
---

# 开闭原则 (The Open/Closed Principle)

- [英文维基百科](https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle)
- [中文维基百科](https://zh.wikipedia.org/wiki/%E5%BC%80%E9%97%AD%E5%8E%9F%E5%88%99)

> 实体应开放扩展并关闭修改。

[SOLID](./solid.md) 的第二个原则。这个原则指出实体（可以是类、模块、函数等）应该能够使它们的行为易于扩展，但是它们的扩展行为不应该被修改。

举一个假设的例子，想象一个能够将 Markdown 转换为 HTML 的模块。如果可以扩展模块，而不修改内部模块来处理新的 markdown 特征，而无需修改内部模块，则可以认为是开放扩展。如果用户不能修改处理现有 Markdown 特征的模块，那么它被认为是关闭修改。

这个原则与面向对象编程紧密相关，让我们可以设计对象以便于扩展，但是可以避免以意想不到的方式改变其现有对象的行为。

## [[架构的整洁之道]] 中的表述

最初由 Bertand Meyer 在 1988 年提出

最初描述:
**设计良好的计算机软件应该易于扩展, 同时抗拒修改**

换句话描述: "**一个设计良好的计算机系统应该在*不需要修改的前提*下就可以轻易被扩展**"

OCP 原则的主要目的是让系统易于扩展, 同时**限制器每次被修改所影响的范围**. 实现方式是通过将系统划分为一些列组件, 并且将这些组件间的**依赖关系按层次结构进行组织**, 使得**高阶组件**不会因为**低阶组件被修改而受到影响**.

## 参见

- [Object-Orientated Programming](#todo)
- [[solid|SOLID]]

