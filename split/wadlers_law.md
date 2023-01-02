---
aliases:
- 沃德勒定律
- Wadler's Law
category:
- 方法论
- hacker-law
name: Wadler's Law
tag:
- 沃德勒定律
- 沃德勒
zhname: 沃德勒定律
id: 20220703234320_769e62f8760d40c0
---

# 沃德勒定律 (Wadler's Law)

- [英文在线地址](https://wiki.haskell.org/Wadler's_Law)

> 任何语言设计中，讨论下面列表中某个要素所花费的总时间与其位置成正比。
>
> 0. 语义 (Semantics)
> 1. 语法 (Syntax)
> 1. 词法 (Lexical syntax)
> 1. 注释语法 (Lexical syntax of comments)
>
> （简而言之，在语义上花费一个小时，就要在注释语法上花费八个小时）。

与 [[the_law_of_triviality|帕金森琐碎定理]] 类似, 沃德勒定律指出，在设计语言时，与这些特征的重要性相比，花在语言结构上的时间过多。

参见：

- [[the_law_of_triviality|帕金森琐碎定理]]

