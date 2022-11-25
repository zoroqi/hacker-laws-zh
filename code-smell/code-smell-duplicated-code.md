---
category:
- 代码的坏味道
aliases:
- Duplicated Code
- 重复代码
name: Duplicated Code
zhname: 重复代码
tags:
- 程序/范例
- 程序/设计
- 代码的坏味道
id: 20221125191747_8692d7629ddd4652
date: "2022-11-25"
---

# Duplicated Code (重复代码)

臭味行列中首当其冲的就是Duplicated Code。如果你在一个以上的地点看到相同的程序结构，那么当可肯定：设法将它们合而为一，程序会变得更好。

最单纯的Duplicated Code就是「同一个class内的两个函数含有相同表达式（expression）」。这时候你需要做的就是采用Extract Method提炼出重复的代码，然后让这两个地点都调用被提炼出来的那一段代码。

另一种常见情况就是「两个互为兄弟〔sibling）的subclasses内含相同表达式」。要避免这种情况，只需对两个classes都使用Extract Method，然后再对被提炼出来的代码使用 Pull Up Field，将它推入superclass内。如果代码之 间只是类似，并非完全相同，那么就得运用Extract Method将相似部分和差异部分割开，构成单独一个函数。然后你可能发现或许可以运用Form Template Method获得一个Template Method设计模式。如果有些函数以不同的算法做相同的事，你可以择定其中较清晰的一个，并使用Substitute Algorithm将其他函数的算法替换掉。

如果两个毫不相关的classes内出现Duplicated Code，你应该考虑对其中一个使用Extract Class，将重复代码提炼到一个独立class中，然后在另一个class内 使用这个新class。但是，重复代码所在的函数也可能的确只应该属于某个class， 另一个class只能调用它，抑或这个函数可能属于第三个class，而另两个classes应该引用这第三个class。你必须决定这个函数放在哪儿最合适，并确保它被安置后就不会再在其他任何地方出现。
