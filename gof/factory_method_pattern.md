---
aliases:
- Factory Method pattern
- 工厂方法模式
category:
- 设计模式
name: Factory Method pattern
tags:
- 设计模式/创建范例
- 工厂方法模式
- 程序/范例
wiki: https://en.wikipedia.org/wiki/Factory_Method_pattern
zhname: 工厂方法模式
zhwiki: https://zh.wikipedia.org/wiki/%E5%B7%A5%E5%8E%82%E6%96%B9%E6%B3%95%E8%8C%83%E4%BE%8B
id: 20221001222431_687aac73c56d4903
date: "2022-10-01"
---

# 工厂方法模式

定义一个用于创建对象的接口，让子类决定实例化哪一个类。FactoryMethod使一个类的实例化延迟到其子类

适用性场景:
* 当一个类不知道它所必须创建的对象的类的时候。
* 当一个类希望由它的子类来指定它所创建的对象的时候。
* 当类将创建对象的职责委托给多个帮助子类中的某一个，并且你希望将哪一个帮助子类是代理者这一信息局部化的时候。

效果:
工厂方法不再将与特定应用有关的类绑定到你的代码中。代码仅处理Product接口；因此它可以与用户定义的任何ConcreteProduct类一起使用。工厂方法的一个潜在缺点在于客户可能仅仅为了创建一个特定的ConcreteProduct对象，就不得不创建Creator的子类。当Creator子类不必需时，客户现在必然要处理类演化的其他方面；但是当客户无论如何必须创建Creator的子类时，创建子类也是可行的。

下面是FactoryMethod模式的另外两种效果：
1. 为子类提供挂钩（hook）用工厂方法在一个类的内部创建对象通常比直接创建对象更灵活。FactoryMethod给子类一个挂钩以提供对象的扩展版本。在Document的例子中，Document类可以定义一个称为CreateFileDialog的工厂方法，该方法为打开一个已有的文档创建默认的文件对话框对象。Document的子类可以重定义这个工厂方法以定义一个与特定应用相关的文件对话框。在这种情况下，工厂方法就不再抽象了而是提供了一个合理的缺省实现。
2. 连接平行的类层次迄今为止，在我们所考虑的例子中，工厂方法并不往往只是被Creator调用，客户可以找到一些有用的工厂方法，尤其在平行类层次的情况下。