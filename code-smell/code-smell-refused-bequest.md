---
category:
- 代码的坏味道
aliases:
- Refused Bequest
- 被拒绝的遗赠
- 被拒绝的遗贈
name: Refused Bequest
zhname: 被拒绝的遗赠
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125190414_4c6ceee85550465c
date: "2022-11-25"
---

# Refused Bequest (被拒绝的遗赠)

Subclasses 应该继承superclasses的函数和数据。但如果它们不想或不需要继承，又该怎么办呢？它们得到所有礼物，却只从中挑选几样来玩！

按传统说法，这就意味继承体系设计错误。你需要为这个subclass 新建一个兄弟（sibling class），再运用Push Down Method 和 Push Down Field 把所有用不到的函数下推给那兄弟。这样一来superclass就只持有所有subclasses共享的东西。常常你会听到这样的建议：所有superclasses都应该是抽象的（abstract）。

既然使用「传统说法」这个略带贬义的词，你就可以猜到，我们不建议你这么做，起码不建议你每次都这么做。我们经常利用subclassing手法来复用一些行为，并发现这可以很好地应用于日常工作。这也是一种坏味道，我们不否认，但气味通常并不强烈。所以我们说：如果Refused Bequest引起困惑和问题，请遵循传统忠告。但不必认为你每次都得那么做。十有八九这种坏味道很淡，不值得理睬。

如果subclass复用了superclass的行为（实现），却又不愿意支持superclass的接口，Refused Bequest的坏味道就会变得浓烈。拒绝继承superclass的实现，这一点我们不介意；但如果拒绝继承superclass的接口，我们不以为然。不过即使你不愿意继承接口，也不要胡乱修改继承体系，你应该运用Replace Inheritance with Delegation 来达到目的。

参考 [[the_liskov_substitution_principle|里氏替换原则]]
