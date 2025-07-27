---
id: e1e2575a-e2c4-42cb-ab31-0dfcc6ae0435

url: https://chatgpt.com/c/6718bbda-cb1c-8010-8eb1-3ffaa11350d3
status:
---


tags:: 

# 计算P(R)的过程
#Omnivore

[Read on Omnivore](https://omnivore.app/me/p-r-192b8ff79a5)
[Read Original](https://chatgpt.com/c/6718bbda-cb1c-8010-8eb1-3ffaa11350d3)

这个多维高斯积分的结果可以通过将其分解为多个一维积分来推导。下面是详细的推导步骤。

### 推导步骤：

考虑积分：

I\=∫dq′exp⁡(−12q′TAq′)I = \\int \\mathrm{d}\\boldsymbol{q}' \\exp\\left(-\\frac{1}{2} \\boldsymbol{q}'^T A \\boldsymbol{q}'\\right)

其中 AA 是一个 n×nn \\times n 的正定对称矩阵。

#### 第一步：对称矩阵的特征值分解

由于 AA 是对称的，我们可以进行特征值分解，得到：

A\=QΛQTA = Q \\Lambda Q^T

其中 QQ 是正交矩阵，Λ\\Lambda 是对角矩阵，其对角元素为 AA 的特征值 λ1,λ2,…,λn\\lambda\_1, \\lambda\_2, \\ldots, \\lambda\_n。

#### 第二步：改变变量

通过变量变换 q′\=Qy\\boldsymbol{q}' = Q \\boldsymbol{y}，则有：

dq′\=dy\\mathrm{d}\\boldsymbol{q}' = \\mathrm{d}\\boldsymbol{y}

因此，积分变为：

I\=∫dyexp⁡(−12(Qy)TA(Qy))I = \\int \\mathrm{d}\\boldsymbol{y} \\exp\\left(-\\frac{1}{2} (Q\\boldsymbol{y})^T A (Q\\boldsymbol{y})\\right)

根据特征值分解，可以得到：

\=∫dyexp⁡(−12yTΛy)\= \\int \\mathrm{d}\\boldsymbol{y} \\exp\\left(-\\frac{1}{2} \\boldsymbol{y}^T \\Lambda \\boldsymbol{y}\\right)

由于 Λ\\Lambda 是对角矩阵，可以写为：

\=∫dy1…dynexp⁡(−12∑i\=1nλiyi2)\= \\int \\mathrm{d}y\_1 \\ldots \\mathrm{d}y\_n \\exp\\left(-\\frac{1}{2} \\sum\_{i=1}^n \\lambda\_i y\_i^2\\right)

#### 第三步：分离积分

将高斯积分分开：

I\=∏i\=1n∫dyiexp⁡(−12λiyi2)I = \\prod\_{i=1}^n \\int \\mathrm{d}y\_i \\exp\\left(-\\frac{1}{2} \\lambda\_i y\_i^2\\right)

对于一维高斯积分：

∫dyexp⁡(−12λy2)\=2πλ\\int \\mathrm{d}y \\exp\\left(-\\frac{1}{2} \\lambda y^2\\right) = \\sqrt{\\frac{2\\pi}{\\lambda}}

因此，对于所有的维度 ii 来说，得到：

I\=∏i\=1n2πλi\=(2π)n/2∏i\=1n1λi\=(2π)n/21det⁡ΛI = \\prod\_{i=1}^n \\sqrt{\\frac{2\\pi}{\\lambda\_i}} = (2\\pi)^{n/2} \\prod\_{i=1}^n \\frac{1}{\\sqrt{\\lambda\_i}} = (2\\pi)^{n/2} \\frac{1}{\\sqrt{\\det \\Lambda}}

#### 第四步：连接 det⁡A\\det A

由 det⁡A\=det⁡(QΛQT)\=det⁡(Q)det⁡(Λ)det⁡(QT)\=det⁡(Λ)\\det A = \\det (Q \\Lambda Q^T) = \\det(Q) \\det(\\Lambda) \\det(Q^T) = \\det(\\Lambda)（因为 QQ 是正交矩阵，det⁡(Q)\=1\\det(Q) = 1），因此：

I\=(2π)n/21det⁡AI = (2\\pi)^{n/2} \\frac{1}{\\sqrt{\\det A}}

最终，我们得到的结果是：

I\=(2π)ndet⁡AI = \\sqrt{\\frac{(2\\pi)^n}{\\det A}}

这个推导完成了多维高斯积分的结果。

