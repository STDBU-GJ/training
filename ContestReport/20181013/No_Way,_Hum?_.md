### Info
* 英文队名  No Way,Hum?
* 中文队名  钱已到位
* 队员1     刘茜童
* 队员2     廖茂均
* 队员3     孙林壮

### 比赛地址
http://acm.sdibt.edu.cn/vjudge/contest/view.action?cid=2099#overview

### 做出来的题目
	A B C D E F

#### A

* 题意
T组输入，给十个数的序列，寻找第三大的数

* 思路
sort一遍，输出第三大的数


#### B

* 题意
给定n个数的一个序列，对这个序列进行划分，使得每个划分的序列的和尽可能的小，求最小的这个数。

* 思路
暴力循环。外层循环是序列的个数从1到n，内层是寻找这样连续的序列是否存在，如果存在，直接break出来，输出该序列的和。


#### C

* 题意
给你给b个球和一栋高为m的楼，问你用最优的策略来判断最坏的情况，最少需要扔几次。
判断方式是：假设先在第k层扔一个球，若球碎了，则再用一个球从k-1层到第1层进行测试;若是没碎，则从第k+1层到第m层进行测试。

* 思路

记忆化找出所有的情况，对于每一种策略，用最坏的情况作为该策略的评判标准，凭此找出最优的策略。


#### D

* 题意
动态的中位数，每输入一个下标为奇数的数，输出到目前为止所有数的中位数。

* 思路
每到下标为奇数的数，sort一遍，输出中位数。



#### E

* 题意
给定一串由十进制组成的串，输出一个串，要求输出的串的字符要和输入串的内容一样，顺序可以不一样，且输出的串需要是最小的大于原串，
的串。如果没有这样的额串，输出“BIGGEST”。

* 思路
直接调用C++的函数，该函数求当前串的下一个排列，如果这样的串不存在，返回 -1 。



#### F

* 题意
给两个值，分别代表串的长度的和该长度的串的函数值，函数值已有题意给出，输出有几个这样的不同的串。

* 思路
暴力循环找长度为i的序列所有的可能情况会很耗时，但是对于长度为i的串的结尾，要么为1,要么为0,且长度为i+1的串的值是由长度为i的串所决定，因此dp搞很轻松。开一个三维数组，分别代表字符串的长度，该串的函数值，和该串结尾的值是零还是一。

### 补的题目


#### H

* 题意
给出凸包的最外侧的点，求凸包圈起来的y轴的长度，和对于每一个被圈起来的y值，输出最左侧的点的x轴坐标和最右侧的点的x轴坐标

* 思路
正在做，thinking......



#### I

* 题意
题目首先规定了一种结构，如题所示，外侧由6个字母组成，要求他们通过中间空的点进行调度，使最后的排列为以特定点为起点，序列按字母序排列，输出最少的调动次数，如果不能形成这样的序列，输出 “NO SOLUTION ”.

* 思路
正在做，thinking......







