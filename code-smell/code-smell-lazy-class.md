---
category:
- 代码的坏味道
aliases:
- Lazy Class
- 冗赘的元素
- 冗赘类
name: Lazy Class
zhname: 冗赘的元素
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125190130_2a06a25f68cb4fc2
date: "2022-11-25"
---

# Lazy Class (冗赘的元素)

你所创建的每一个class，都得有人去理解它、维护它，这些工作都是要花钱的。如 果一个class的所得不值其身价，它就应该消失。项目中经常会出现这样的情况： 某个class原本对得起自己的身价，但重构使它身形缩水，不再做那么多工作；或开发者事前规划了某些变化，并添加一个class来应付这些变化，但变化实际上没 有发生。不论上述哪一种原因，请让这个class庄严赴义吧。如果某些subclass没有做满足够工作，试试 Collapse Hierarchy。对于几乎没用的组件，你应该以Inline Class对付它们。
