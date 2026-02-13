---
tags:
  - math
  - math/数学分析
projects: 未完成
---
>[!question] 问题
>若$\exists N \in \mathbb{N}$, 使得对于任意的$n>N$成立$x_n ≥ y_n$，
>能推出$\inf\limits_{n>N} x_n \ge \sup\limits_{n>N} y_n$吗?

这里关键是对于上确界和下确界的理解: 
上确界是上界的最小元素: 
设序列$\{x_n\}$的上确界为$a$, 上界为$\{a_n\}$, 
一种定义为: $a := \left(\forall x_n(a \ge x_n)\right) \cap \left(\forall m < a,\exists x_n(x_n > m)\right)$

$\inf\limits_{n > N}{x_n} \ge \sup\limits_{n > N}{y_n}$
= **从某个 $N$ 之后，${x_n}$ 的整个尾部都在 ${y_n}$ 的整个尾部之上**



