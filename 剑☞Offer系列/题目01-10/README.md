#### 01 二维数组的查找（Easy，数组）
> 此题目为有序二维数组查找问题，判断该二维数组中是否含有某个目标整数。  
我们从最右上角元素开始查找判断，若该元素比目标整数小，则该行剩余元素均比目标小，下移一位；反之则该列剩余元素均比目标大，左移一位，直至找到目标元素或行列的某一下标越界。

#### 02 替换空格（Easy，字符串）
> 此题目为将一个字符串（char\*）中的所有空格**原地**替换为`%20`，不得定义另一辅助数组。  
首先我们计算字符串中有多少个空格，得到新字符串的长度，将字符串中原有字符逐个后移。

#### 03 从尾到头打印链表（Medium，链表，递归（回溯））
> 注意是**从尾到头**打印，我么可以利用递归或是回溯的算法思想，在回溯的过程中将值存放在一个全局数组里面。

#### 04 重建二叉树（Medium，树，递归）
> 此题目为根据一棵树的“前序遍历”和“中序遍历”结果（假设不含重复元素），重建该二叉树。  
通过简单的递归可以解决，注意“前序遍历”的第一个元素即为根节点元素，“中序遍历”又根据根节点将结果分为左子数“中序遍历”和右子数“中序遍历”，这样便可以从根开始重构二叉树。

#### 05 用两个栈实现队列（Easy，栈和队列）
> 此题目为用两个栈（stack，先进后出FILO）实现队列（queue，先进先出FIFO）的功能。  
见代码，略。

#### 06	旋转数组的最小数字（Easy，查找和排序，二分查找（Binary Search））
> 此题目为寻找一个旋转数组中的最小数字。  
通过遍历查找不满足递增顺序的接点处数字，算法复杂度为O(n)；可以利用二分查找Binary Search将算法复杂度优化为O(logn)，见代码。

#### 07 斐波那契数列（Easy，斐波那契）
> 简单利用斐波那契数列的生成规则，`f[n] = f[n-1] + f[n-2], f[0] = 0, f[1] = 1` 

#### 08 跳台阶（Medium，递归）
> 此题目为青蛙一次可以跳1级也可以跳2级台阶，问跳上一个n级台阶共有多少种跳法。  
我们通过递归来解决此题，两个基础情况`n=1`和`n=2`，然后通过递归统计两种情况的跳法之和。

#### 09 变态跳台阶（Medium，递归，贪心，循环）
> 此题目为青蛙一次可以跳1级也可以跳2级也可以跳n级台阶，问跳上一个n级台阶共有多少种跳法。    
我可以发现`f(n) = 1（直接跳） + f(n-1) + f(n-2) + ... + f(1)`，因此可以用简单的循环来解决此问题，代码较长但容易理解；另一种通过递归实现贪心，我们发现规律`f(1) = 1, f(2) = 2, f(3) = 4, f(4) = 8, ... `即`f(n) = 2*f(n-1)`，当`n=1`时返回`1`，代码简洁。

#### 10 矩形覆盖（Medium，递归，斐波那契）
> 此题目为用`2*1`的矩形去覆盖一个`2*n`的大矩形总共有多少种方法。  
试几个例子发现：`f(0) = 0, f(1) = 1, f(2) = 2, f(3) = 3, f(4) = 5, ...`从`n=2`开始，有点斐波那契数列的意思，然后就可以了。
 
