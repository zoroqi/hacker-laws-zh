---
category:
- 代码的坏味道
aliases:
- Middle Man
- 中间转手人
name: Middle Man
zhname: 中间人
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125185141_697155e6a38541d7
date: "2022-11-25"
---

# Middle Man (中间转手人)


对象的基本特征之一就是封装（encapsulation）——对外部世界隐藏其内部细节。封装往往伴随 delegation （委托）。比如说你问主管是否有时间参加一个会议，他就把这个消息委托给他的记事簿，然后才能回答你。很好，你没必要知道这位主管到底使用传统记事簿或电子记事簿抑或秘书来记录自己的约会。

但是人们可能过度运用delegation。你也许会看到某个class接口有一半的函数都委托给其他class，这样就是过度运用。这时你应该使用Remove Middle Man，直接和实责对象打交道。如果这样「不干实事」的函数只有少数几个，可以运用 Inline Method 把它们" Inlining"，放进调用端。如果这些Middle Man还有其他行 为，你可以运用 Replace Delegation with Inheritance 把它变成实责对象的subclass，这样你既可以扩展原对象的行为，又不必负担那么多的委托动作。

