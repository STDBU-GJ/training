# 近期学习内容的一个简要总结

## effective c++
读了一半多了，了解了很多以前不知道或者说是从来不会去考虑的东西。
印象比较深的一点是异常安全那一部分，每一条语句的顺序都得精心考虑，否则会造成严重的后果。总结有一下三点：
1. 异常安全函数要保证即使发生异常，也不会泄漏资源，或造成数据结构败坏，并且拥有三种保证之一(基本承诺，强烈保证，不抛出异常保证）。
2. 强烈保证往往能够以cas（copy-and-swap）实现，但并非对所有函数都可实现或具备现实意义(资源消耗较大)。
3. 函数提供的异常安全保证，通常最高只等于其所调用的各个函数的异常安全保证的最弱者。
4. 尽量使用RAII管理资源。

## 计算机网络
这个没细看，b站看了个微视频，看了一半，相当于快速过一遍。

## 操作系统
快速过了一遍哈工大的课，算是对整体框架有个大致的了解。
然后现在在看ostep和jyy的操作系统课(感觉讲的很好，至少讲的比较现代,就是有点喜欢炫技)。

计划看完ostep后看csapp(有时间的话）。

## cmu15445
目前做了p0,p1,p2。暂时放下了，同时做太多事有点兼顾不过来。
### p0
主要是测试基本的并发编程(一把大锁闯天下)和c++11的熟练度，要求不是很高，也就移动语义和智能指针用的多一点，(对我来说挺高的)。
然后要求主要是实现一个cow字典树(某个群友简历上写了这个，面试官问他什么是奶牛字典树),这是一种优化策略，适用于读较多的程序。
读时共享数据，写时会copy一个副本给调用者。

### p1
实现一个buffer pool，比较良心，注释写的还算全(看的懂英文的花，机翻的真不能看！)，还给你提供了disk manager接口，不用自己实现，不然会被折磨死。
**task1**:实现LRUKReplacer，访问次数到k的遵循LRU替换策略，未到k的遵循FIFO替换策略。
**task2**：实现buffer pool manager。
**task3**：实现read/write page guard。这个是一个管理资源的类，自动处理资源和锁，省的程序员操心。
整体来看p1不难(只加大锁的情况下）,不用考虑太多并发问题。

### p2
这是整个lab中最难的一个projeck了,没有注释，给的都是空类和一些可能你会用到的类成员，一切都只能自己设计，而且不能大锁闯天下了。鬼知道我被deadlock折磨了多久。
实现b+树，没有借鉴其他b+树的实现，单纯看原理实现了B+树 还是挺开心的，虽然写的是依托答辩(能跑就行)。
具体不细说了。

剩下两个project  后面空了再写。
