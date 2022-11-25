---
category:
- 代码的坏味道
aliases:
- Inappropriate Intimacy
- 狎昵关系
name: Inappropriate Intimacy
zhname: 狎昵关系
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125191743_b382b6e3ce4246c8
date: "2022-11-25"
---

# Inappropriate Intimacy (狎昵关系)

有时你会看到两个classes过于亲密，花费太多时间去探究彼此的private成分。如果这发生在两个「人」之间，我们不必做卫道之士；但对于classes，我们希望它们严守清规。

就像古代恋人一样，过份狎昵的classes必须拆散。你可以采用 Move Method 和 Move Field 帮它们划清界线，从而减少狎昵行径。你也可以看看是否运用 Change Bidirectional Association to Unidirectional 让其中一个class对另一个斩断情丝。如果两个实在是情投意合，可以运用Extract Class 把两者共同点提炼到一个安全地点，让它们坦荡地使用这个新class。或者也可以尝试运用 Hide Delegate 让另一个class来为它们传递相思情。

继承（inheritance）往往造成过度亲密，因为subclass对superclass的了解总是超过superclass的主观愿望。如果你觉得该让这个孩子独自生活了，请运用Replace Delegation with Inheritance 让它离开继承体系。
