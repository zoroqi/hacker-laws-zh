---
category:
- 代码的坏味道
aliases:
- Parallel Inheritance Hierarchies
- 平行继承体系
name: Parallel Inheritance Hierarchies
zhname: 平行继承体系
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125183816_6ad68006244e4470
date: "2022-11-25"
---

# Parallel Inheritance Hierarchies (平行继承体系)


Parallel Inheritance Hierarchies其实是shotgun surgery的特殊情况。在这种情况下，每当你为某个class增加一个subclass，必须也为另一个class相应增加一个subclass。如果你发现某个继承体系的名称前缀和另一个继承体系的名称前缀完全相同，便是闻到了这种坏味道。

消除这种重复性的一般策略是：让一个继承体系的实体（instance）指涉（参考、引用、refer to）另一个继承体系的实体(instances)。如果再接再厉运用Move Method 和 Move Field，就可以将指涉端（ referring class ）的继承体系消弭于无形。

