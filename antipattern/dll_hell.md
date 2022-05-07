---
aliases:
- "DLL hell"
- "DLL地狱"
name: "DLL hell"
zhname: "DLL地狱"
zhwiki: "https://zh.wikipedia.org/wiki/DLL%E5%9C%B0%E7%8B%B1"
groups: "配置管理"
category:
- 反面模式
- antipattern
- 方法论
---

# DLL地狱

* [wiki:DLL地狱](https://zh.wikipedia.org/wiki/DLL%E5%9C%B0%E7%8B%B1)

不同版本DLL所带来的问题，包括DLL可见性和多版本问题，在微软的Windows上尤为突出

在电脑运算领域，DLL地狱（DLL Hell）指Microsoft Windows系统中，因为动态链接库（DLL）的版本或兼容性的问题而造成软件无法正常执行。

Windows早期并没有很严谨的DLL版本管理机制，以致经常发生安装了某软件后，因为其覆盖了系统上原有的同一个DLL文件，而导致原有可运行的程序无法运行。但还原回原有的DLL文件之后，所新安装的软件就无法运行。若影响到系统所使用的重要DLL时也可能让系统容易死机甚至无法正常启动。

在一般情况下，开发时修改了类中的成员变量的大小或者改变虚函数的个数以及顺序会触发DLL地狱。

如果DLL重新发布时类成员（虚函数表也属于类成员）的地址发生变化，那也会触发DLL地狱

* [[dependency_hell|依赖地狱]]