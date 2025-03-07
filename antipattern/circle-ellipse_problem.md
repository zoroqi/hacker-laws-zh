---
aliases:
- Circle-ellipse problem
- 圆还是椭圆问题
name: Circle-ellipse problem
zhname: 圆还是椭圆问题
groups: 面向对象设计
category:
- 反面模式
- antipattern
- 方法论
id: 20220703234330_0d2102519c2c4d2c
---

# 圆还是椭圆问题


基于变量的子类化关系进行子类化.

[圆还是椭圆问题](https://en.wikipedia.org/wiki/Circle%E2%80%93ellipse_problem)（有时称为正方形矩形问题）说明了在物件建模中使用子类型多态性时可能出现的几个陷阱。这些问题在使用面向对象（OOP）时最常遇到。根据定义，这个问题违反了 [[solid|SOLID]] 原则之一的[[the_liskov_substitution_principle|里氏替换原则]]。

问题涉及表示圆和椭圆（或类似的，正方形和矩形）的类别之间应该存在哪种子类型或继承关系。更一般地，该问题说明了当基类包含以某种方式改变对象的方法时可能出现的困难，这种方式可能会使派生类中发现的（更强的）不变量无效，从而导致违反里氏替换原则。
