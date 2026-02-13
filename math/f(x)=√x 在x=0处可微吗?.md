---
tags:
  - math
  - math/Calculus_微积分
projects: 未完成
---

>[!question] 问题
>$f(x)=\sqrt{x}$在$x=0$处可微吗?

>[!note] 命题
>函数的可微性是一个很好的性质, 它说明了函数局部可以被线性函数逼近
>单变量函数 $f$ 在点 $a$ 处**可微**当且仅当存在常数 $L$（即 $f'(a)$）使得$$f(a+h)=f(a)+L\,h+o(h)\qquad(h\to0)$$
>其中$o(h)$是对于逼近的误差$R(h)$满足当对任意的$\varepsilon>0$存在一个$\delta_{\varepsilon,x_0}>0$使得当$|h|<\delta_{\varepsilon,x_0}$的时候都有$$|R(h)|<\varepsilon h$$
>也就是$$|\dfrac{R(h)}{h}-0|<\varepsilon$$
>为什么是要求$|\dfrac{R(h)}{h}-0|<\varepsilon$?误差可以任意小不就够了吗?(即$|R(h)-0|<\varepsilon$), 见[[关于Chain Rule的证明]]


设$f(x)=\sqrt{x}$在$x=0$处的导数为$f^{'}(0)\,(记为L)$,
则有: $$f(0+h)=f(0)+Lh+o(h)\qquad (h \to 0)$$








>[!question] 应用
>问题1: 
>(a) 记$|x|=\sqrt{x^2}$, 证明: $$\frac{\mathrm{d}}{\mathrm{d}x}|x|=\frac{x}{|x|}$$
>(b) 如果$f(x)=|\sin{x}|$, 求$f^{'}(x)$并画出$f$和$f^{'}$的粗略图像. $f$在何处不可微?
>(c) 如果$f(x)=|\sin{x}|$, 求$f^{'}(x)$并画出$f$和$f^{'}$的粗略图像. $f$在何处不可微?

