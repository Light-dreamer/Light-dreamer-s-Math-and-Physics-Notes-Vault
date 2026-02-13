---
tags:
  - math
  - tool_idea
  - math/数学分析
projects: 未完成
---
分析学的一个核心idea
【【如何学习数分】一个核心的想法】 https://b23.tv/dA9PPrP
请用自己的话和理解写作, 不要抄袭

举例：![[Pasted image 20251029200706.png]]比夹逼定理更深刻，



### 
>[!note] 命题0.1
>$$\forall \varepsilon>0,x<a+\varepsilon\implies x\leq a$$
证明: 依据实数连续性, 任意一个实数如果满足$x>a$, 那么一定存在一个${\varepsilon}_0$, 使得 $x \ge a + {\varepsilon}_0$
实际上左右两个命题就是等价的, $x \leq a$ 的话, 一定有$\forall \varepsilon>0, a+\varepsilon > x$
#### 例1- [[关于极限的单调性定理的证明]]
在[[关于极限的单调性定理的证明]]中, 我们将$y_n<x_n$且两序列极限存在, 证明$\lim\limits_{n \to \infty}y_n \le \lim\limits_{n \to \infty}x_n$的问题等价为了证明$\forall \varepsilon>0,\lim\limits_{n \to \infty}y_n < \lim\limits_{n \to \infty}x_n + \varepsilon$
这换来了可将$\lim\limits_{n \to \infty}y_n$ 放大为$n$足够大时的$y_n+\dfrac{\varepsilon}{2}$的操作空间, 进而将$y_n$放大为$x_n+\dfrac{\varepsilon}{4}$, 再对$n$足够大时的$x_n$放大至$\lim\limits_{n \to \infty}x_n + \dfrac{\varepsilon}{4}$

### 
#### 例- [[关于极限的单调性定理的证明#引申 夹逼定理/夹逼准则|关于夹逼定理的证明]]
在[[关于极限的单调性定理的证明#引申 夹逼定理/夹逼准则|关于夹逼定理的证明]]中, 对于$x_n>y_n$, $y_n$极限存在且与$x_n$的极限相同, 也就是在$n$足够大时$x_n,y_n$之间的距离$x_n-y_n=o(1)$
