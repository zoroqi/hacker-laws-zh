---
category:
- 代码的坏味道
- 反面模式
- antipattern
aliases:
- Shotgun Surgery
- 霰弹式修改
- 霰弹枪手术
name: Shotgun Surgery
zhname: 霰弹式修改
wiki: https://en.wikipedia.org/wiki/Shotgun_surgery
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20220703231440_2063be5e8e5c4485
date: "2022-11-25"
---

# Shotgun Surgery (霰弹式修改)

开发人员一次性在一个多个实现的代码基中增加功能

Shotgun Surgery类似[[code-smell-divergent-change|发散式变化]]，但恰恰相反。如果每遇到某种变化，你都必须在许多不同的classes内做出许多小修改以响应之，你所面临的坏味道就是Shotgun Surgery。如果需要修改的代码散布四处，你不但很难找到它们，也很容易忘记某个重要的修改。

这种情况下你应该使用Move Method 和 Move Field 把所有需要修改的代码放进同一个class。如果眼下没有合适的可以安置这些代码，就创造一 个。通常你可以运用Inline Class 把一系列相关行为放进同一个class。这可能会造成少量Divergent Change，但你可以轻易处理它。

Divergent Change是指「一个class受多种变化的影响」，Shotgun Surgery则是指「一种变化引发多个classes相应修改」。这两种情况下你都会希望整理代码，取得「外界变化」与「待改类」呈现一对一关系的理想境地。
