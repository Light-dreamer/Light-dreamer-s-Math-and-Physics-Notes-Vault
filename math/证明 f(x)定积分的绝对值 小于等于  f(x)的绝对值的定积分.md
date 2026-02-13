---
tags:
  - math
  - math/Calculus_微积分
---

[[连续函数的性质总结|连续函数的性质总结 性质 2. 连续函数的绝对值仍是连续函数]]


>[!question] 问题
>证明定积分的一个性质: $$\int_a^b |f(x)| \,\mathrm{d}x \ge |\int_a^b f(x)\,\mathrm{d}x|$$


>[!note] 想法
>我们之所以感觉$$\int_a^b |f(x)| \,\mathrm{d}x \ge |\int_a^b f(x)\,\mathrm{d}x|$$是因为$|f(x)|$一定都在$x$轴上, 而$f(x)$并不都在$x$轴上. 在积分时$|f(x)|$会一直累加, 而$|\int_a^b f(x)\,\mathrm{d}x|$在积分时则要将$f(x)$自己的正数部分 ($|f(x)|$)与负数部分 ($- |f(x)|$)进行中和
>
>所以 $|f(x)|$的定积分一定比 $|\int_a^b f(x)\,\mathrm{d}x|$大
>
>图像上来说, 就类似于这种: 
>![[证明 f(x)定积分的绝对值 小于等于  f(x)的绝对值的定积分.png]]
>
>运用了[[分而治之|分而治之_整体的感觉可微分到 每个部分都 来证明]]这一tool_idea



证明过程: 
由不等式: $$|f(x)| \ge f(x) \ge - |f(x)|$$
得到$$\int_a^b |f(x)|\,\mathrm{d}x \ge \int_a^b f(x)\,\mathrm{d}x \ge -\int_a^b |f(x)|\,\mathrm{d}x$$
此即 $$\int_a^b |f(x)| \,\mathrm{d}x \ge |\int_a^b f(x)\,\mathrm{d}x|$$
定积分的这个性质 (指: $\int_a^b |f(x)| \,\mathrm{d}x \ge |\int_a^b f(x)\,\mathrm{d}x|$)和不等式$|a+b| \le |a|+|b|$相当, 也可以从定积分定义直接证明