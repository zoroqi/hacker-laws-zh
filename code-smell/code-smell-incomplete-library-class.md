---
category:
- 代码的坏味道
aliases:
- Incomplete Library Class
- 不完美的程序库类
name: Incomplete Library Class
zhname: 不完美的程序库类
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125192118_fa60865941064af0
date: "2022-11-25"
---

# Incomplete Library Class (不完美的程序库类)

复用（reuse）常被视为对象的终极目的。我们认为这实在是过度估计了（我们只是使用而己）。但是无可否认，许多编程技术都建立在library classes （程序库类）的基础上，没人敢说是不是我们都把排序算法忘得一干二净了。

library classes构筑者没有未卜先知的能力，我们不能因此责怪他们。毕竟我们自己也几乎总是在系统快要构筑完成的时候才能弄清楚它的设计，所以library 构筑者的任务真的很艰巨。麻烦的是library的形式（form）往往不够好，往往不可能让我们修改其中的classes使它完成我们希望完成的工作。这是否意味那些经过实践检验的战术如 Move Method 等等，如今都派不上用场了？

幸好我们有两个专门应付这种情况的工具。如果你只想修改library classes内的一两 个函数，可以运用 Introduce Foreign Method；如果想要添加一大堆额外行为，就得运用Introduce Local Extension。

