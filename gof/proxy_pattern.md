---
aliases:
- Proxy pattern
- 代理模式
category:
- 设计模式
name: Proxy pattern
tags:
- 设计模式/结构范例
- 代理模式
- 程序/范例
wiki: https://en.wikipedia.org/wiki/Proxy_pattern
zhname: 代理模式
zhwiki: https://zh.wikipedia.org/wiki/%E4%BB%A3%E7%90%86%E6%A8%A1%E5%BC%8F
id: 20221001230713_798d1a907fb14258
date: "2022-10-01"
---

# 代理模式

为其他对象提供一种代理以控制对这个对象的访问

适用性场景:

在需要用比较通用和复杂的对象指针代替简单的指针的时候，使用Proxy模式。下面是一些可以使用Proxy模式常见情况：
1. 远程代理（RemoteProxy）为一个对象在不同的地址空间提供局部代表。NEXTSTEP Add94 使用NXProxy类实现了这一目的。Coplien Cop92称这种代理为“大使”（Ambassador）。
2. 虚代理（VirtualProxy）根据需要创建开销很大的对象。在动机一节描述的ImageProxy就是这样一种代理的例子。
3. 保护代理（ProtectionProxy）控制对原始对象的访问。保护代理用于对象应该有不同的访问权限的时候。例如，在Choices操作系统 CIRM93 中KemelProxies为操作系统对象提供了访问保护。
4. 智能指引（SmartReference）取代了简单的指针，它在访问对象时执行一些附加操作。它的典型用途包括：
    * 对指向实际对象的引用计数，这样当该对象没有引用时，可以自动释放它(也称为SmartPointers Ede92)。
    * 当第一次引用一个持久对象时，将它装入内存。
    * 在访问一个实际对象前，检查是否已经锁定了它，以确保其他对象不能改变它。

效果:

Proxy模式在访问对象时引入了一定程度的间接性。根据代理的类型，附加的间接性有多种用途：
1. RemoteProxy可以隐藏一个对象存在于不同地址空间的事实。
2. VirtualProxy可以进行最优化，例如根据要求创建对象。
3. ProtectionProxies和SmartReference都允许在访问一个对象时有一些附加的内务处理（Housekeepingtask）。

Proxy模式还可以对用户隐藏另一种称之为copy-on-write的优化方式，该优化与根据需要创建对象有关。拷贝一个庞大而复杂的对象是一种开销很大的操作，如果这个拷贝根本没有被修改，那么这些开销就没有必要。用代理延迟这一拷贝过程，我们可以保证只有当这个对象被修改的时候才对它进行拷贝。

在实现Copy-on-write时必须对实体进行引用计数。拷贝代理仅会增加引用计数。只有当用户请求一个修改该实体的操作时，代理才会真正的拷贝它。在这种情况下，代理还必须减少实体的引用计数。当引用的数目为零时，这个实体将被删除。

Copy-on-Write可以大幅度的降低拷贝庞大实体时的开销。