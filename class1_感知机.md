20171202 qzd
# 机器学习算法入门之感知机 #
主要内容：
1、python基本介绍
2、感知机算法推导
3、简单的编程实践


## 一、python基本介绍 ##
- python 3.x
- Numpy:用于数值计算的库
- Matplotlib:为了可视化，用于输出图像

## 二、感知机算法推导 ##
### 1、大脑神经元 ###
![](https://i.imgur.com/vPpOcgD.png)

### 2、典型的感知机结构 ###
![](https://i.imgur.com/Rn66uZ3.png)

- &nbsp; xo w0,使用偏置的原因？  
XW不过原点，让其超平面在坐标任意位置画圈。

### 3、激活函数 ###
![](https://i.imgur.com/WHcsQis.png)

- 最常见是Sigmoid
- 激活函数最主要因素是给系统引入非线性。（很多问题是非线性，而典型感知器的图中求和是线性组合，模拟不了非线性问题）
- ReLU是CNN中用到的激活函数。

### 4、如何确定权重（weight）？ ###
- 首先，定义目标函数object function（误差函数error function，损失函数loss function）这里用E表示。
 - 误差函数有很多定义方法，比如二乘误差、交叉熵误差。
- 有了误差以后，就是一个误差最小化的问题。我们的目的是使得最终的计算结果和实际情况的误差最小。最理想的情况就是没有误差，即E=0。

![](https://i.imgur.com/AtsJPG0.png) 

- <font color=red size=4 face="黑体">任务：找出E最小是的W。</font>
- 方法：梯度下降法。
![](https://i.imgur.com/gX6zcJp.png)
 - 需要思考的问题：蓝色的小人怎么走才会最快的到达红色爱心的方向，而避免走紫色这条偏离路线。
 - 首先从二维角度进行分析。
 ![](https://i.imgur.com/adnujlL.png)
   - 任务：到达目标的点。
   - 首先任选取一点，斜率为负往正方向移动，斜率为正往反方向移动。梯度下降法原理，移动的方向是斜率的反方向。当达多维角度则运用到梯度概念，这也就是为什么叫梯度下降法的原因。
   - <font color=red size=4 face="黑体">如何更新权重？</font>
    ![](https://i.imgur.com/93IimU7.png)
<img src="http://latex.codecogs.com/gif.latex?Wi=Wi-\eta\sum_{k=1}^{n}(W(k)X(k)-t(k))Xi" title="Wj=Wj-\eta\sum_{k=1}^{n}(W(k)X(k)-t(k))Xj" />

### <font color=red size=5 face="黑体"> 5、感知机算法流程图 </font>###
![](https://i.imgur.com/sb8Ffm8.png)

## 三、简单的程序实践 ##
![](https://i.imgur.com/VIrxoWs.png)

![](https://i.imgur.com/KW1zm6s.png)
