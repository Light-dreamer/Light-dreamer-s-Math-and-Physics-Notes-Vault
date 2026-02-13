---
tags:
  - math/数列
  - math/数学分析
projects: 未完成
aliases:
  - 对于足够大的n,两个实的序列满足x_n ≥ y_n 是否能够说明 对于足够大的n, {X_N} 包含 {Y_N} 呢?
---
>[!question] 问题1
>若$\exists N \in \mathbb{N}$, 使得对于任意的$n>N$成立$x_n ≥ y_n$, 且两个序列收敛
>能否推出$\inf\limits_{n > N}{x_n} \ge \sup\limits_{n > N}{y_n}$?

$\inf\limits_{n > N}{x_n} \ge \sup\limits_{n > N}{y_n}$
= **从某个 $N$ 之后，${x_n}$ 的整个尾部都在 ${y_n}$ 的整个尾部之上**
### 问题2
[[x_n>y_n能说明inf{x_n}>sup{y_n}吗?]]

### 问题3
>[!question] 问题2
>若$\exists N \in \mathbb{N}$, 使得对于任意的$n>N$成立$x_n ≥ y_n$，
>能否推出$\lim_{n → \infty} \inf{x_n} \ge \lim_{n → \infty} \sup{y_n}$?

想到$x_n=\dfrac{\sin n}{n}$的图像, 
这个时候, 你是不能说所有的$x_n$尾部整体一定大于$y_n$的尾部整体, 比如这个图像: ![[所有的x_n这个整体 ≥ 所有的y_n整体吗?.png]]
再比如
### 反例
考虑序列：
\[
x_n = 1 + (-1)^n = \begin{cases}
0, & n \text{为奇数}, \\
2, & n \text{为偶数},
\end{cases}
\quad
y_n = (-1)^n = \begin{cases}
-1, & n \text{为奇数}, \\
1, & n \text{为偶数}.
\end{cases}
\]
对任意 \(n\)，有 \(x_n \geq y_n\)：
- 当 \(n\) 为奇数时，\(0 \geq -1\)；
- 当 \(n\) 为偶数时，\(2 \geq 1\)。

但
\[
\liminf_{n \to \infty} x_n = 0, \quad \limsup_{n \to \infty} y_n = 1,
\]
因此 \(0 \geq 1\) 不成立。


#### 附加说明
当 ($\{y_n\}$) 收敛时，有 ($\liminf y_n = \limsup y_n$)，此时可得 ($\liminf x_n \geq \limsup y_n$)。但在一般情况下，该结论不成立。

---

>[!question] 问题2
>若$\exists N \in \mathbb{N}$, 使得对于任意的$n>N$成立$x_n ≥ y_n$，
>设$\mathrm{X_N}=[\inf\limits_{n > N}{x_n}, \sup\limits_{n>N}{x_n}],\mathrm{Y_N}=[\inf\limits_{n > N}{y_n}, \sup\limits_{n>N}{y_n}]$, 
>是否能够推出$\{X_N\} \supset \{Y_N\}$?


---

