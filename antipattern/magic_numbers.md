---
aliases:
- Magic numbers
- 魔术数字
name: Magic numbers
zhname: 魔术数字
zhwiki: https://zh.wikipedia.org/wiki/%E9%AD%94%E8%A1%93%E6%95%B8%E5%AD%97_(%E7%A8%8B%E5%BC%8F%E8%A8%AD%E8%A8%88)
groups: 编程
category:
- 反面模式
- antipattern
- 方法论
id: 20220703233646_04d2230dc554429c
---

# 魔术数字

* [wiki:魔术数字](https://zh.wikipedia.org/wiki/%E9%AD%94%E8%A1%93%E6%95%B8%E5%AD%97_(%E7%A8%8B%E5%BC%8F%E8%A8%AD%E8%A8%88))

在算法里直接使用数字，而不解释含义

在程序设计中，魔术数字（magic number）可能指：

* 缺乏解释或命名的独特数值。常常在程序中出现多次，并且可以（从规范上而言也应当）被有名字的常量取代。
* 用于识别一个文件格式或协议类型的一段常量或字符串，例如UNIX的特征签名。
* 不易于其他值混淆的值，例如UUID。
