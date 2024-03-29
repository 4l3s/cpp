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

引用折叠与完美转发
https://www.zhihu.com/question/40346748




## 操作系统：
内存分配:
https://www.cnblogs.com/myseries/p/12487211.html
分段解决问题：
1地址空间不隔离
2程序运行时候的地址不确定
因为分段提出了一个虚拟地址的概念
## 操作系统实战45讲
彭东
操作系统的分页是一种内存管理技术，它将物理内存划分为固定大小的块，称为页框，同时将逻辑地址空间划分为相同大小的页。当程序需要访问内存时，它会生成一个虚拟地址，操作系统会将这个虚拟地址转换为物理地址，然后将数据从物理内存中读取出来。

分页的主要优点是它可以将物理内存分配给多个进程，从而实现更高效的内存利用。此外，分页还可以提高系统的安全性，因为每个进程只能访问自己的页，而不能访问其他进程的页。

分页的实现需要硬件和软件的支持。硬件需要提供一个页表，用于将虚拟地址转换为物理地址。软件需要实现页表的管理和维护，以及处理页错误等异常情况。


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


https://blog.csdn.net/qq_35034604/article/details/107959429

## GPU
http://www.3fun.net/575/
## mysql
https://xiaolincoding.com/mysql/transaction/phantom.html#%E6%80%BB%E7%BB%93
间歇锁
写，读如何保证一致性

## cpp金典问题
https://blog.csdn.net/qq_35034604/article/details/107959429

## 小工具
https://quick-bench.com/q/Nd-_MgmOpYTDHsEqMbI5w1BROQk

信号传输的原理
https://www.zhihu.com/question/35769259

jvm
https://zhuanlan.zhihu.com/p/351216320

线程和cpu核心的关系
https://www.zhihu.com/question/274189552
CPU的核心数和线程数量是什么关系？ - Java面试365的回答 - 知乎
https://www.zhihu.com/question/274189552/answer/2359390179

## Java基础知识
公平锁：每个线程获取锁的顺序是按照线程访问锁的先后顺序获取的，最前面的线程总是最先获取到锁。

非公平锁：每个线程获取锁的顺序是随机的，并不会遵循先来先得的规则，所有线程会竞争获取锁。
## presto基础知识
codegen
https://cloud.tencent.com/developer/article/1054862

分布式一致性算法

presto的调度算法

https://mayunlei.github.io/2020/05/30/Presto-%E4%BB%BB%E5%8A%A1%E8%B0%83%E5%BA%A6%EF%BC%9A-%E4%BB%BB%E5%8A%A1%E5%88%86%E9%85%8D%E5%88%B0%E5%93%AA%E9%87%8C/

 shuffer的过程
 
 cbo优化器
 
 https://www.cnblogs.com/JasonCeng/p/14199298.html
 https://mayunlei.github.io/2020/05/30/Presto-%E4%BB%BB%E5%8A%A1%E8%B0%83%E5%BA%A6%EF%BC%9A-%E4%BB%BB%E5%8A%A1%E5%88%86%E9%85%8D%E5%88%B0%E5%93%AA%E9%87%8C/
 
 hive的存储
 
 presto基础知识，详细读
 https://zhuanlan.zhihu.com/p/54385845
 
 mysql里面的多并发
 
 pdp本地鉴权也要去数据库查询，如何做到大量请求的。
 
 内存泄漏问题定位以及裁内存
 
 分布式limit分析
 
 https://zhuanlan.zhihu.com/p/57030465
 
 presto的coordinator节点不参与计算，final阶段，partial阶段都是在worker节点上计算，
 
 ## presto
 
 https://zhuanlan.zhihu.com/p/345733460
 
 ## redis
 
 https://blog.csdn.net/qq_22155255/article/details/121871167
  ## tcp
  tcp三次握手
  第三次失败，会发生什么。连接池
## kafka学习
  https://www.cnblogs.com/Jcloud/p/17510848.html
  
## 海量数据
 https://wangpengcheng.github.io/2019/12/17/hailiangshuju_problems/
 
 ## 数据倾斜
 https://zhuanlan.zhihu.com/p/332368318
 ## 刷题
 
 46.全排列	https://leetcode.cn/problems/permutations/ 
 47.全排列II	 https://leetcode.cn/problems/permutations-ii/
 784.字母大小写全排列	 https://leetcode.cn/problems/letter-case-permutation/
 字符串的排列	 https://leetcode.cn/problems/zi-fu-chuan-de-pai-lie-lcof/
 77.组合	 https://leetcode.cn/problems/combinations/
 39.组合总和	 https://leetcode.cn/problems/combination-sum/
 40组合总和II	 https://leetcode.cn/problems/combination-sum-ii/
 216.组合总和III	 leetcode.cn/problems/combination-sum-iii/
 377.组合总和IV	 https://leetcode.cn/problems/combination-sum-iv/
 78.子集	 https://leetcode.cn/problems/subsets/
 90.子集II	 https://leetcode.cn/problems/subsets-ii/

## 书籍
血酬定律
 http://wx0313.free.fr/book/5.pdf
## 分布式一致性算法
 https://www.cnblogs.com/xybaby/p/10124083.html
 https://zhuanlan.zhihu.com/p/91288179
 https://juejin.cn/post/6907151199141625870
 https://raft.github.io/
 https://cloud.tencent.com/developer/article/1739489
 资源调度算法去学习一下
 ## 小孩子的书
 https://www.zhihu.com/question/605640833?utm_division=hot_list_page
 ## 工作相关
 https://www.zhihu.com/question/382390653
 iam
 https://zhuanlan.zhihu.com/p/454018164
