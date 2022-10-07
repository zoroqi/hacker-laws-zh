---
aliases:
- Adapter pattern
- 适配器模式
category:
- 设计模式
name: Adapter pattern
tags:
- 设计模式/结构范例
- 适配器模式
- 程序/范例
wiki: https://en.wikipedia.org/wiki/Adapter_pattern
zhname: 适配器模式
zhwiki: https://zh.wikipedia.org/wiki/%E9%80%82%E9%85%8D%E5%99%A8%E6%A8%A1%E5%BC%8F
id: 20221001231136_a350c1ab34ef4d07
date: "2022-10-01"
---

# 适配器模式

将一个类的接口转换成客户希望的另外一个接口。 Adapter 模式使得原本由于接口不兼容而不能一起工作的那些类可以一起工作.

适用性场景:
* 你想使用一个已经存在的类，而它的接口不符合你的需求。
* 你想创建一个可以复用的类，该类可以与其他不相关的类或不可预见类（即那些接口可能不一定兼容的类）协同工作。
* （仅适用于对象 Adapter）你想使用一些已经存在的子类，但是不可能对每一个都进行子类化以匹配它们的接口。对象适配器可以适配它的父类接口。

类适配器和对象适配器有不同的权衡
* 用一个具体的Adapter类对Adaptee和Target进行匹配。结果是当我们想要匹配一个类以及所有它的子类时，类Adapter将不能胜任工作。
* 使得Adapter可以重定义Adaptee的部分行为，因为Adapter是Adaptee的一个子类。
* 仅仅引入了一个对象，并不需要额外的指针以间接得到adaptee。对象适配器则
* 允许一个Adapter与多个Adaptee—即Adaptee本身以及它的所有子类（如果有子类的话）—同时工作。Adapter也可以一次给所有的Adaptee添加功能。
* 使得重定义Adaptee的行为比较困难。这就需要生成Adaptee的子类并且使得Adapter引用这个子类而不是引用Adaptee本身。
