---
tags:
  - math
  - math/函数/函数图像
  - math/Calculus_微积分
projects: 未完成
---

>[!question] 问题
> We have found the derivatives of $x^2 + y^2 = 4$ and $x^4 + y^4 = 16$ respectively to be $y'=-\dfrac{x}{y}$,$y'=-(\dfrac{x}{y})^3$, respectively.
> The graph below shows the curve $x^4 + y^4 = 16$.![[a fat circle - 曲线x的4次方+y的4次方=1.png]]Notice that it’s a stretched and flattened version of the circle $x^2 + y^2 = 4$.(And that's why it is called a fat circle), By the derivative of $x^4+y^4=16$ and $x^2 + y^2 = 4$, try to explain the reason. 

We can first use $y'=-\dfrac{x}{y}$ to see why $x^2 + y^2 = 4$ is a circle. 
	不难看出$x^2 + y^2 = r^2$的导数均为$y'=-\dfrac{x}{y}$
由$x^2 + y^2 = r^2$可以直接的看出$x,y$的取值范围均为$[-r,r]$(因为二者对称且平方数不会小于$0$), 也就是他们在以$O$为中心边长为$r$的正方形内![[以O为中心边长为r的正方形.png]]
我们有了4个定点$(r,0),(-r,0),(0,r),(0,-r)$并且知道这也分别对应了曲线在$x$轴,$y$轴上的所有点
由这四个定点结合$y'=-\dfrac{x}{y}$在这个正方形内绘图
由$y'=-\dfrac{x}{y}$我们可以观察到|y'|的大小取决于|x|与|y|之间的大小关系, 由此想到以|y|=|x|的点所在的直线为参照, 依此对$|x|$和$|y|$大小关系区域进行划分![[以y的绝对值=x的绝对值的点所在的直线为参照, 依此对x绝对值和y绝对值大小关系区域进行划分.png]]
	上图中: 
	蓝线上的点|x|=|y|;
	绿色区域内的点|y|>|x|(以|y|=|x|的点所在的直线为参照, 在x不动的情况下(垂直于x轴方向上移动)增大|y|;
	黄色区域内的点|x|>|y|(以|x|=|y|的点所在的直线为参照, 在y不动的情况下(垂直于y轴方向上移动)增大|x|.
则曲线在蓝线上的点|y'|=1, 绿色区域内的点|y'|>1, 黄色区域内的点|y'|<1
而$(r,0),(-r,0),(0,r),(0,-r)$这4个特殊定点则是将|y'|拉到了极致
	曲线在$(r,0),(-r,0)$处的|y'|=\infty(其实不可微)
	曲线在$(0,r),(0,-r)$处的|y'|=0

下面演示了由$(r,0)$出发演绎到$(0,r),(0,-r)$的图像(实际能演绎出一个圆,这里只演绎了一半)
 ![[由曲线的点(r,0)结合导数信息演绎曲线图像.png]]
 而且已经演绎的第一,四象限里曲线的轨迹只可能有这一条, 若非如此, 曲线在$x$轴上将不只经过$(\pm r,0)$

我们来看$x^4+y^4=r^4$
