# 编号：588
---

![[Pasted image 20251125213434.png]]
**解题思路**：判断一个数是否**包含数字9**，需要检查它的**每一位数字**是否等于9
![[Pasted image 20251125213523.png]]




# 编号：590
---

![[Pasted image 20251125213744.png]]
**解题思路**：这个序列是卡特兰数
**通项公式：**
![[Pasted image 20251125215258.png]]
设卡特兰数第n项位h(n)
**递推：因为项数较少可以直接递推出来，就不用公式了

**规律：** 第一个一定是一对括号，这对括号中可以有括号(h0~n)，可以没括号(h0)，则这对括号外 * 余下括号对数
![[Pasted image 20251126145711.png]]

# 编号：605
---

![[Pasted image 20251126144422.png]]
**解题思路**： 十进制转任意进制都是类似模版，重要的是注意余数应该为0 + "A"

![[Pasted image 20251126144515.png]]
**或者使用Excel**
![[Pasted image 20251126145140.png]]
=SUBSTITUTE(ADDRESS(1, A1, 4), "1", "")
![[Pasted image 20251126145312.png]]
![[Pasted image 20251126145319.png]]


# 编号：143
---

![[Pasted image 20251126151354.png]]

方法一：
这数学公式，这个有点像**离散数学和初等数论，反正不是算法的范畴
![[Pasted image 20251126151622.png]]
方法二：推荐，直接就过程枚举出来了，搞什么O(1)想上面怎么多
![[Pasted image 20251126152556.png]]

# 编号：624
----

![[Pasted image 20251129144046.png]]

**==本题考点是三角形基本公式，没有算法思维==**
对于顶点的三角形面积公式： 底乘高除2 （平行四边形面积的一半）
$$
S=1/2∣(x2​−x1​)(y3​−y1​)−(x3​−x1​)(y2​−y1​)∣
$$
![[Pasted image 20251129150335.png]]
<span style="background:#b1ffff">INCIDENTALLY</span>：这个顶点公式看着是不是像向量叉积：
$$
平行四边形面积=∣AB×AC∣=∣(x2​−x1​)(y3​−y1​)−(x3​−x1​)(y2​−y1​)∣
$$
![[Pasted image 20251129150638.png]]
![[Pasted image 20251129151924.png]]



# 编号：97
---

![[Pasted image 20251128112537.png]]
这个题如果用暴力枚举一定会超，时间复杂度为:

$$
O(N²)
$$
使用**前缀和 + 同余定理 + 哈希统计**，时间复杂度为**O(N)**:


**什么是前缀和**：该数组的每个元素表示原始数列**从开始位置**到**当前位置**的所有元素之和。
**什么是同余数**：定义--设整数 𝑚 ≠0![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7 "m\ne0")。若 𝑚 ∣(𝑎 −𝑏)![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7 "m\mid(a-b)")，称 𝑚![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7 "m") 为 **模数**（**模**），也就是说如果a % m == b % m，那么 a-b 一定是m的**整除数**
**什么是哈希统计**：就是哈希表

![[Pasted image 20251128214146.png]]
**优化：**
![[Pasted image 20251128215607.png]]


# 编号：99
---
## ![[Pasted image 20251129111259.png]]**这个题目的核心思想**：找到最大的边长(L)，让每个小朋友(总K)都能获得最大巧克力，总共是K 个 L×L 的小正方形

	本题在蓝桥的测试平台上，用枚举和二分的测试用例最低都能达到1ms，比赛用枚举是最优解题效率；而二分对比枚举，二分是时间效率是最优的。
**解题思路**：
![[Pasted image 20251129141930.png]]枚举：时间复杂度 -- O(n * maxL)   当 **n 很大**，或者 **巧克力的边长 maxL 很大** 时，枚举法会超时
![[Pasted image 20251129142233.png]]
二分：时间复杂度：O(n × log(maxL))  `log` 指的是 **以 2 为底的对数（log₂）**
![[Pasted image 20251129142330.png]]

