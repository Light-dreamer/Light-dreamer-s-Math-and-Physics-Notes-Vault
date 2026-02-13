---
tags:
  - math
  - math/Calculus_微积分
  - math/LinearAlgebra_线性代数
projects: 未完成
---
>[!tip] 核心想法

>[!note] 这能否加深你对分析学,微积分或线性代数的理解和认识?

---
>[!question] 问题1.0
>用函数极限的$\varepsilon-\delta$定义证明$\lim\limits_{x \to 3}x^2=9$

(这个Question后还有一个延伸问题: 
>[!question] 问题1.1
>为什么$\delta$不能取大于等于$\varepsilon$比$6$的值？


>[!note] 问题1.0的思路总结
>由于$y=x^2$的变化率由原点出发向两边越来越快, 我们只取与$\varepsilon$成比例的$\delta$无法确保$\varepsilon$较大时对$x$到估计点的距离对应的函数值都在$(L-\varepsilon,L+\varepsilon)$中, 通过限制$\delta=\min\{\text{确切的正实数},\text{与}\varepsilon\text{成比例的值}\}$, 确保当$\varepsilon$较大时, 我们有一个至少的限制: $x$到估计点的距离至少小于那个确切的正实数 使得对应的函数值仍在$(L-\varepsilon,L+\varepsilon)$范围内. 
>
>这里需要注意的是: $x$到估计点的距离至少小于那个确切的正实数 是我们自己主动加上去的(譬如: 令$0<|x-3|<1$), 敢这么干是因为$|x^2-9|<\varepsilon$可拆分为$|x+3||x-3|<\varepsilon$, 我们可以将这个主动加的限制放在$|x+3|$上, 再使不等式中的另一个$|x-3|$在这个主动加的限制的基础上满足$|x+3||x-3|<\varepsilon$, 得到对$x$到$3$距离的另一个限制
>最后只要确保两者能同时满足, 即取使$x$到$3$的距离更小的那个值, 数学语言来描述就是 $\delta=\min\{\text{确切的正实数},\text{与}\varepsilon\text{成比例的值}\}$


 "用函数极限的定义($\varepsilon-\delta$语言)证明$\lim\limits_{x \to 3}x^2=9$" 
用函数极限的定义证明函数$f(x)=x^2$在$x=3$处的极限为$9$, 
即用$\delta$限制$x$到$3$的范围, 使这个范围内的$x$($x=3$除外)满足函数值可以任意的接近$9$
用合适的符号(这里用$\varepsilon-\delta$语言)来描述这个命题, 题设为: $\forall \varepsilon>0, \exists \delta, \text{使满足}0<|x-3|<\delta的$$x$满足 结论 为: $|x^2-9|<\varepsilon$
观察到结论中有和题设相同的东西, 可将结论转化为$|x-3||x+3|<\varepsilon$

随着$\varepsilon$的变化$\delta$要作出响应, $\delta$依赖于$\varepsilon$, 先将$\varepsilon$看作一个固定的数, 去猜测使命题成立的$\delta$的值
 
其中$|x-3|<\delta \implies |x-3||x+3|<\delta|x+3|$, 
我们想把$|x+3|$换掉, 因为它是不确定的, 我们想把它换成一个确定的数
我们肯定是要把$|x+3|$替换掉, 而且也只能是通过$\delta$对的限制得出它小于一个数进而把它替换掉, 我们不想将$|x+3|$替换成含$\delta$的式子, 因为这样最后用来证明命题的$x$的范围取的不太好(最后要解的会是常数项含$\varepsilon$的关于的二次及以上的式子, 其解一定含有带$\varepsilon$的根式, 也就是: 证明命题的$x$的取值范围不太好吗????我自己也有些不确定, 需要请教专业人士). 

既然, 将$|x+3|$替换成含$\delta$的式子不太行(最后要解的会是常数项含$\varepsilon$的关于$\delta$的二次及以上的式子, 其解一定含有带$\varepsilon$的根式), 那$|x+3|$能否替换成,换言之,使其小于一个确切的数呢?只能通过对的性质得出它小于一个数进而把它替换掉. 问题就转化为了我们可否限制$|x-3|$小于一个确切的数呢?
应该是可以的, 我们讲函数极限时在意的只是这个点附近的行为(在这里, 我们只对$3$附近的$x$感兴趣), 所以可以设(到3的距离)小于一个合适的数(比如让, 也就是让)
$0<|x-3|<1 \implies x<4 \implies |x+3|<7$, $|x+3|<7$

可得: $|x-3||x+3|<7 \cdot \delta \le \varepsilon$
可知$\delta=\dfrac{\varepsilon}{7}$

你会发觉我们猜测的使命题成立的$\delta$有两个值, 这是为什么呢?
$\delta=1$这个取值是我们限制$|x-3|<1$, 
$\delta=\dfrac{\varepsilon}{7}$取值是我们让$7\delta=\varepsilon$, 这里的$7\delta=\varepsilon$又是为什么? 使$7|x-3|<\varepsilon$. 也就是: 实际上$\delta$的作用还是限制$|x-3|< \dfrac{\varepsilon}{7}$. 

到这里, 你也不难发觉在函数极限中, $\delta$的取值就是为了限制$x$到估计点的可取范围. 

那么我们只需同时满足这两个对$|x-3|$的限制即可, 让$\delta=\min\{1, \dfrac{\varepsilon}{7}\}$. 

猜测完$\delta$的可取值后, 我们要证明这个$\delta$可行, 下面给出证明过程. 

给定$\varepsilon>0$, 令$\delta=\min\{1, \dfrac{\varepsilon}{7}\}$. 
$|x-3|<1 \implies x<4 \implies |x+3|<7$
则$|x^2-9|=|x-3||x+3|<7|x-3|$
再利用$0<|x-3|<\dfrac{\varepsilon}{7}$, 
可得$|x^2-9|<7|x-3|<7\cdot\dfrac{\varepsilon}{7}=\varepsilon.$ 
这表明 $\lim\limits_{x \to 3}=9$. 

回顾: 我们最后是通过让$\delta=\min\{1, \dfrac{\varepsilon}{7}\}$来证明命题成立的, 我们看到$\delta=\min\{1, \dfrac{\varepsilon}{7}\}$可能会有些奇怪, 这里的$\delta=\min\{1, \dfrac{\varepsilon}{7}\}$怎么理解?我们可以找几个$\varepsilon$的值代进去看看, 发觉$\delta=\min\{1, \dfrac{\varepsilon}{7}\}$限制这我们拿来作估计的$x$到$3$的距离必须小于$1$, 同时, 当$\varepsilon$足够小时, $\delta$再次作出响应, 调整拿来作估计的$x$到$3$的距离必须小于$\dfrac{\varepsilon}{7}$, 这是一种动态的感觉


>[!question] Question
>为什么$\delta$不能取大于等于$\varepsilon$比$6$的值？

这里要先注意这个问题的讨论前提是我们已经限制$\delta$至少要小于一个正实数了, $\dfrac{\varepsilon}{n}$这种是在$\varepsilon$较小时取到的, 也就是, 我们讨论的是$y=x^2$在点$(3,9)$的极附近的行为

1. 这个问题是否正确?
	直观的判断, 我们只取$x=3$附近的极小的一段函数图像, 它接近于一条直线$y=6x$, 而实际上, $y=x^2$的右侧的变化率要比$6$快, 由$\varepsilon:\delta=6:1$的比例并不能达到被$\delta$限定的$x$对应的函数值都在$(6-\varepsilon, 6+\varepsilon)$中. $\delta$($x$到$3$的距离)取的更大时就更不可能了. 
	
	注: 并非不看$x=3$的左侧, 而是左侧的变化率比$6$慢, 用$6$的比例的限定左侧一定能达到精度要求. 所以我们只用看变化率更快的右侧即可

总结: 从根本上来说这来自于直线的对称(这也是为什么直线中有定比分点) 以及 抛物线的不对称??(泽风)

但我们不应满足于此, 这只是直观上的判断, 我们还需要严谨的证明和验证它, 

先验证$\delta=\dfrac{\varepsilon}{6}$时它限定范围内得到的函数值可以大于$9+\varepsilon$
代入$x-3=\delta=\dfrac{\varepsilon}{6}$到$y=x^2$中, 预测得到的应该是比$9+\varepsilon$大的值, $$\begin{align}
x-3=\dfrac{\varepsilon}{6} \implies x&=3+\dfrac{\varepsilon}{6}\\
\text{当} x=3+\dfrac{\varepsilon}{6}\text{时},y&=x^2=(3+\dfrac{\varepsilon}{6})^2=9+\varepsilon+\dfrac{{\varepsilon}^2}{36}
\end{align}$$
由实数连续性可知$\exists x\in(3,3+\delta)\left(x^2>9+\varepsilon\right)$ 
这个是我们由$3$的极附近得到的(我们可以想象$y=x^2$在点$(3,9)$的变化率$\to$稍微往右一点点的变化率的增长是极微小的), 因此我们猜测只要限制$x$到$3$的距离比$\dfrac{\varepsilon}{6}$小一点点, 就能满足$\forall 0<|x-3|<\delta\left(9-\varepsilon<x^2<9+\varepsilon\right)$

我们可以先代入一个数试试, 这里代入$x=3+\delta=3+\dfrac{\varepsilon}{6.001}$
得到$$\begin{align}x^2=(3+\dfrac{\varepsilon}{6.001})^2&=9+\dfrac{6\varepsilon}{6.001}+\dfrac{{\varepsilon}^2}{{6.001}^2}\\
x^2-(9+\varepsilon)&=-\dfrac{0.001\varepsilon}{6.001}+\dfrac{{\varepsilon}^2}{{6.001}^2}\end{align}$$
我们知道自己讨论的是$\varepsilon$较小($\varepsilon<1$)时的$\delta$对$x$到$3$的距离的限定
可以想见, 此时$\dfrac{{\varepsilon}^2}{{6.001}^2}$要比$\dfrac{0.001\varepsilon}{6.001}$小, 也就是$x^2<9+\varepsilon$

严格的证明就是给定任意的$m>0$取$\delta=\dfrac{\varepsilon }{6+m}$, 有$x^2<9+\varepsilon$(用取$x=3+\dfrac{\varepsilon }{6+m}$时的函数值比$9+\varepsilon$来说明), 根据上面的例子我们可以预测最后应该是$x^2-(9+\varepsilon)=-\dfrac{m\varepsilon}{6+m}+\dfrac{{\varepsilon}^2}{{6+m}^2}$

后面的应该和上面的例子一样, 这里就不往下算了, 
我们得到了只要限制$x$的右侧到$3$的距离小于$1:6$的比例, 我们就能满足精度要求

这个结论是可以简要论证的

在点$(3,9)$附近, 
由于$y=x^2$从中心点$O$往两边的增长速率越来越快,在$x=3$附近是严格单调的,  $x>3$时的变化率$>$ $x=3$时的变化率 $>$ $x<3$时的变化率, 而且变化率的变化并非突变. 那么我们只需要关心限定$x=3$的右侧附近到$x=3$的距离就可以满足要求, 而$y=x^2$的变化是连续的, 它在$x>3$时的变化率只比$6$大了一点点, 所以我们只需要限制它到$3$的距离比函数值到$9$的距离的值小于$1:6$即可. 



当然, 这个问题还有另一种解答视角, 是从对$|x+3||x-3|$的解读出发的, 
我们仍是讨论的$\varepsilon$较小的情况(只有此时我们才取$\delta$为与$\varepsilon$成比例的值)
此时仍是一样的, 我们应当关心的是$x=3$的右侧附近的情况, 也即取$x>3$, 则$|x+3|$应当大于$6$, 如果我们取$|x+3|$小于$6$, 那我们只是在对$x<3$的情景进行讨论, 在该情境下由$|x+3||x-3|$得到的$|x-3|$应受到的限制是基于已经限定$x<3$得到的, 那这个限制必然是不能对整个情景成效的. 
所以我们应当是在限定$x>3$也就是先限定$|x+3|>6$的情境下由$|x+3||x-3|$得到的$|x-3|$应受到的限制, 此时得出的$\delta$与$\varepsilon$的比值一定小于$1:6$. 

Q：从几何角度验证用于证明..的最大的delta是根号下（9+epsilon） -3
