---
aliases:
- "Poltergeists"
- "幽灵"
name: "Poltergeists"
zhname: "幽灵"
zhwiki: "https://zh.wikipedia.org/wiki/%E5%B9%BD%E7%81%B5_(%E5%8F%8D%E9%9D%A2%E6%A8%A1%E5%BC%8F))"
groups: "面向对象设计"
category:
- 反面模式
- antipattern
- 方法论
---

# 幽灵

* [wiki:幽灵](https://zh.wikipedia.org/wiki/%E5%B9%BD%E7%81%B5_(%E5%8F%8D%E9%9D%A2%E6%A8%A1%E5%BC%8F))

指这样一些对象，它们唯一的作用就是把信息传给其它对象

在程式设计中，幽灵（poltergeist）是指一些生命期很短，没有内部状态的物件，这些物件是只用来进行初始化或调用其他生命期较长物件的方法。幽灵是一种反面模式。原始定义是由 Michael Akroyd 于1996年在Object World West Conference中提出：

“这些生命期很短的物件就像幽灵马车或骚灵现象一様，神秘的出现及消失。因此代码变的更难维护，而且其中会有不必要的资源浪费。这类反面模式的典型原因是不好的物件设计。”
幽灵物件常常可以由其名称来识别：例如 "manager_"、"controller_"或"start_process"等。

有时幽灵物件的创建是因为程式设计者预期需要使用一个复杂的架构，例如在命令模式下同一个方法需适用于客户端及调用端，因此程式设计者将其分为二个阶段，只是复杂的架构后来没有实现，只留下幽灵物件。不能将幽灵物件和其他在MVC等设计模式中使用，生命期较长，有状态的物件混为一谈。

若要移除幽灵物件，可直接删除物件，将其机能直接加入要调用幽灵物件的物件中，加入机能的方式可以透过继承或是混入（mixin）的方式。