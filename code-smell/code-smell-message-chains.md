---
category:
- 代码的坏味道
aliases:
- Message Chains
- 过长的消息链
- 过度耦合的消息链
name: Message Chains
zhname: 过长的消息链
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125184902_e082ed2ee1424c79
date: "2022-11-25"
---

# Message Chains (过长的消息链)

如果你看到用户向一个对象索求（request）另一个对象，然后再向后者索求另一个对象，然后再索求另一个对象……这就是Message Chains。实际代码中你看到的可 能是一长串getThis()或一长串临时变量。采取这种方式，意味客户将与查找过程中的航行结构（structure of the navigation）紧密耦合。一旦对象间的关系发生任何变化，客户端就不得不做出相应修改。

这时候你应该使用Hide Delegate。你可以在Message Chains的不同位置进行这种重构手法。理论上你可以重构Message Chains上的任何一个对象，但这么做往往会把所有中介对象（intermediate object ）都变成Middle Man。通常更好的选择是：先观察Message Chains最终得到的对象是用来干什么的，看看能否以 Extract Method 把使用该对象的代码提炼到一个独立函数中，再运用Move Method 把这个函数推入Message Chains。如果这条链上的某个对象有多位客户打算航行此航线的剩余部分，就加一个函数来做这件事。

有些人把任何函数链（method chain。译注：就是Message Chains；面向对象领域中所谓「发送消息」就是「调用函数」）都视为坏东西，我们不这样想。呵呵，我们的冷静镇定是出了名的，起码在这件事情上是这样。

