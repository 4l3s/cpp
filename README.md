# cpp


C++是一种面向对象的编程语言，具有高效、灵活、强大和可移植等特点和优势。

Java是一种纯面向对象的编程语言，而C++是增强型的C语言。

内存泄漏是指程序中申请内存空间但未释放，最终导致系统内存耗尽。解决内存泄漏问题可以通过智能指针、RAII等方法。

多态是指同一操作作用于不同对象，产生不同的行为。例如，多态的一个实例是基类Shape有一个纯虚函数area()，派生类Rectangle和Triangle均实现了area()函数。

虚函数是允许在派生类中重写基类的函数，以实现多态。需要使用虚函数来保证正确的函数调用。

STL(Standard Template Library)是C++标准模板库。STL包含了容器、迭代器、算法和函数对象等组件。

const 关键字可以用于修饰变量、函数参数、函数返回值以及成员函数等，在编译时防止修改。 const 成员函数是指不能修改类的成员变量。

拷贝构造函数用于创建新对象并初始化为另一个同类对象，赋值运算符函数用于对象间赋值。它们的主要区别是赋值函数必须确保不会产生内存泄漏。

模板是一种创建泛型类或函数的工具，可以提高代码重用率和效率。

智能指针是C++11中引入的一种智能管理动态内存的机制，它通过RAII技术自动释放内存并避免内存泄漏。

在C++中用于异常处理的关键字是try、catch、throw。异常处理的优点是可以在程序运行时捕捉并处理错误，缺点是可能产生运行时的额外开销。
https://developer.aliyun.com/article/709155
![image](https://user-images.githubusercontent.com/30437929/229087399-4dc213ec-c795-4dd5-83a6-b02fbfaf4771.png)
http://www.3fun.net/575/
C语言中“指针”和“指针变量”的区别是什么

来自 <https://blog.csdn.net/u011555996/article/details/79496203> 



比较严格的说法是这样的： 
系统为每一个内存单元分配一个地址值，C/C++把这个地址值称为“指针”。如有int i=5;，存放变量i的内存单元的编号(地址)&i被称为指针。 
“指针变量”则是存放前述“地址值”的变量，也可以表述为，“指针变量”是存放变量所占内存空间“首地址”的变量(因为一个变量通常要占用连续的多个字节空间)。比如在int i=5;后有一句int *p=&i;，就把i的指针&i赋给了int *型指针变量p，也就是说p中存入着&i。所以说指针变量是存放指针的变量。 
有一个事实值得注意，那就是有不少资料和教科书并没有如上区分，而是认为“指针是指针变量的简称”，如对int *p=&i;的解释是：声明一个int *型指针p，并用变量i的地址初始化；而严格说应该是声明一个int *型指针变量p才对。所以有时看书要根据上下文理解实质，而不能过于拘泥于文字表述

来自 <https://blog.csdn.net/u011555996/article/details/79496203> 

c++类的大小

https://blog.csdn.net/fengxinlinux/article/details/72836199

为什么要字节对齐
https://cloud.tencent.com/developer/article/1631792
最重要的考虑是提高内存系统性能
对齐原理
https://blog.csdn.net/sweetfather/article/details/78487563

https://zhuanlan.zhihu.com/p/30007037
对于多重继承里面的成员变量还是按照继承顺序来的

虚函数表与虚函数指针
https://cloud.tencent.com/developer/article/1599283

虚函数实现多态的原理
https://blog.csdn.net/zoopang/article/details/14071779?ydreferer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS5oay8%3D






操作系统的理解：
内存分配:
https://www.cnblogs.com/myseries/p/12487211.html
分段解决问题：
1地址空间不隔离
2程序运行时候的地址不确定
因为分段提出了一个虚拟地址的概念


分页解决的问题
 内存使用率低下
 
 ## shell
sh遵循POSIX规范:"当某行代码出错时，不继续往下解释"。bash就算出错，也会继续向下执行。
列子
```shell
sh脚本
#!/bin/sh
source err
echo "test sh"

结果为:
testsh.sh: 2: testsh.sh: source: not found
```
```
bash 脚本:

#!/bin/bash
source err
echo "test sh"

结果为:
testsh.sh: 2: testsh.sh: source: not found
test sh
```
## c++ 多线程

