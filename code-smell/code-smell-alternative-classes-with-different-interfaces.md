---
category:
- 代码的坏味道
aliases:
- Alternative Classes with Different Interfaces
- 异曲同工的类
name: Alternative Classes with Different Interfaces
zhname: 异曲同工的类
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125192147_662ae0d7f6674ea8
date: "2022-11-25"
---

# Alternative Classes with Different Interfaces (异曲同工的类)

如果两个函数做同一件事，却有着不同的签名式（signatures），请运用Rename Method 根据它们的用途重新命名。但这往往不够，请反复运用Move Method 将某些行为移入classes，直到两者的协议（protocols ）一致为止。如果你必须重复而赘余地移入代码才能完成这些，或许可运用Extract Superclass 为自己赎 点罪。
