---
aliases:
- "Hard code"
- "硬编码"
name: "Hard code"
zhname: "硬编码"
zhwiki: "https://zh.wikipedia.org/wiki/%E7%A1%AC%E7%BC%96%E7%A0%81"
groups: "编程"
category:
- 反面模式
- antipattern
- 方法论
---

# 硬编码

* [wiki:硬编码](https://zh.wikipedia.org/wiki/%E7%A1%AC%E7%BC%96%E7%A0%81)

将对系统环境的假设写入实现中

硬编码（英语：Hard Code或Hard Coding）是指在软件实现上，将输出或输入的相关参数（例如：路径、输出的形式或格式）直接以常量的方式撰写在源代码中，而非在执行期间由外界指定的设置、资源、资料或格式做出适当回应。一般被认定是种反模式或不完美的实现，因为软件受到输入资料或输出格式的改变就必须修改源代码，对客户而言，改变源代码之外的小设置也许还比较容易。