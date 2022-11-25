---
category:
- 代码的坏味道
aliases:
- Large Class
- 过大的类
- 过大类
name: Large Class
zhname: 过大的类
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125191833_d224ac9cddd84660
date: "2022-11-25"
---

# Large Class (过大的类)

如果想利用单一class做太多事情，其内往往就会出现太多instance变量。一旦如此，Duplicated Code也就接踵而至了。

你可以运用Extract Class将数个变量一起提炼至新class内。提炼时应该选择class内彼此相关的变量，将它们放在一起。例如"depositAmount"和 "depositCurrency"可能应该隶属同一个class。通常如果class内的数个变量有着相同的前缀或字尾，这就意味有机会把它们提炼到某个组件内。如果这个组件适合作为一个subclass，你会发现Extract Subclass往往比较简单。

有时候class并非在所有时刻都使用所有instance变量。果真如此，你或许可以多次使用Extract Class或Extract Subclass。

和「太多instance变量」一样，class内如果有太多代码，也是「代码重复、混乱、死亡」的绝佳滋生地点。最简单的解决方案（还记得吗，我们喜欢简单的解决方案）是把赘余的东西消弭于class内部。如果有五个「百行函数」，它们之中很多代码都相同，那么或许你可以把它们变成五个「十行函数」和十个提炼出来的「双行函 数」。

和「拥有太多instance变量」一样，一个class如果拥有太多代码，往往也适合使用Extract Class和Extract Subclass。这里有个有用技巧：先确定客户端如何使用它们，然后运用Extract Interface为每一种使用方式提炼出一个接口。这或许可以帮助你看清楚如何分解这个class。

如果你的Large class是个GUI class，你可能需要把数据和行为移到一个独立的领域对象（domain objec）去。你可能需要两边各保留一些重复数据，并令这些数据同步（sync.）。Duplicate Observed Data告诉你该怎么做。这种情况下，特别是如果你使用旧式Abstract Windows Toolkit (AWT)组件，你可以采用这种方式去掉GUI class并代以Swing组件。
