---
category:
- 代码的坏味道
aliases:
- Repeated Switches
- 重复的switch
name: Repeated Switches
zhname: 重复的switch
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125184652_0365584df3d747e8
date: "2022-11-25"
---

# Repeated Switches (重复的switch)

面向对象程序的一个最明显特征就是：少用switch (或case）语句。从本质上说， switch语句的问题在于重复（duplication）。你常会发现同样的switch语句散布 于不同地点。如果要为它添加一个新的子句，你必须找到所有switch语句 并修改它们。面向对象中的多态（polymorphism ）概念可为此带来优雅的解决办法。

大多数时候，一看到switch语句你就应该考虑以「多态」来替换它。问题是态 该出现在哪儿？switch语句常常根据 type code（型别码）进行选择，你要的是「与 该 type code相关的函数或class」。所以你应该使用Extract Method 将switch语句提炼到一个独立函数中，再以Move Method 将它搬移到需要多态性的那个class里头。此时你必须决定是否使用 Replace Type Code with Subclasses 或 Replace Type Code with State/Strategy。一旦这样完成继承结构之后， 你就可以运用Replace Conditional with Polymorphism了。

如果你只是在单一函数中有些选择事例，而你并不想改动它们，那么「多态」就有 点杀鸡用牛刀了。这种情况下Replace Parameter with Explicit Methods是个不错的选择。如果你的选择条件之一是null，可以试试Introduce Null Object。

