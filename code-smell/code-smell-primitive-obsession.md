---
category:
- 代码的坏味道
aliases:
- Primitive Obsession
- 基本类型偏执
- 基本型别偏执
name: Primitive Obsession
zhname: 基本类型偏执
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125191934_4447e630556943e4
date: "2022-11-25"
---

# Primitive Obsession (基本类型偏执)

大多数编程环境都有两种数据：结构型别（record types）允许你将数据组织成有意义的形式；基本型别（Primitive type）则是构成结构型别的积木块。结构总是会带来一定的额外开销。它们有点像数据库中的表格，或是那些得不偿失（只为做一两件事而创建，却付出太大额外开销〕的东西。

对象的一个极具价值的东西是：它们模糊（甚至打破）了横亘于基本数据和体积较大的classes之间的界限。你可以轻松编写出一些与语言内置（基本〕型别无异的小型classes。例如Java就以基本型别表示数值，而以class表示字符串和日期——这 两个型别在其他许多编程环境中都以基本型别表现。

对象技术的新手通常不愿意在小任务上运用小对象——像是结合数值和币别的 money classes 、含一个起始值和一个结束值的range classes、电话号码或邮政编码（ZIP） 等等的特殊strings。你可以运用Replace Data Value with Object 将原本单独存在的数据值替换为对象，从而走出传统的洞窟，进入炙手可热的对象世界。如果欲替换之数据值是 type code（型别码），而它并不影响行为，你可以运用 Replace Type Code with Class 将它换掉。如果你有相依于此 type code的条件式，可运用 Replace Type Code with Subclasses 或 Replace Type Code with State/Strategy 加以处理。

如果你有一组应该总是被放在一起的值域（fields），可运用Extract Class。 如果你在参数列中看到基本型数据，不妨试试Introduce Parameter Object。 如果你发现自己正从array中挑选数据，可运用Replace Array with Object。
