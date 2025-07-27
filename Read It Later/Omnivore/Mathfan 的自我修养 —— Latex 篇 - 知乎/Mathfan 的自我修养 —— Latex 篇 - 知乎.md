---
id: f4896923-023e-4b53-b854-81a323e1d428

url: https://zhuanlan.zhihu.com/p/720441726
---


tags::  #Readed 

# Mathfan 的自我修养 —— Latex 篇 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/mathfan-latex-192031d0b80)
[Read Original](https://zhuanlan.zhihu.com/p/720441726)

---

## 序

那**灵然跃动**的**数学符号**，**跃动**时如**火星**，**恬静**时如**水影**，**提炼**於透视**理性**的**灵魂**。

---

## 前言

使用`Latex` 多年，故打算在此**记录**一些**不成熟**的使用**经验**。

作为一种**信仰**，若能**分享**其中的**奥妙**，又何尝不是一种**乐趣**。

---

ζ(s)\=1Γ(s)∫0∞xs−1ex−1 dx0<ℜ(s)<1\\bbox\[#ACF,20px,border:1px\]{\\zeta(s)= \\frac{1}{\\Gamma(s)}\\int\_0^\\infty\\frac{x^{s-1}}{e^x-1}\\ \\mathrm{d}x\\quad\\quad 0<\\Re(s)<1}\\\\

```tex
\zeta(s)=
\frac{1}{\Gamma(s)}\int_0^\infty\frac{x^{s-1}}{e^x-1}\ \mathrm{d}x\quad\quad
0<\Re(s)<1\\
```

| 符号  | Latex 代码       | 说明              |
| --- | -------------- | --------------- |
| 分式  | \\frac{a}{b}   | 也可用 '\\over'    |
| 积分号 | \\int\_{a}^{b} | 环路积分号用 '\\oint' |
| 微分号 | \\mathrm{d}    | 通常可直接使用 'd'     |
| 空格  | \\quad         | 也可用 '\\ '       |
| 居中  | \\\\           | 也包括换行           |

---

## 自动高度

```scss
\left{[左符号]}{[内容]}\right{[右符号]}
```

该功能**很有用**，比如

```tex
f(x)=\ln(1+\frac{1}{x})\\
```

f(x)\=ln⁡(1+1x)f(x)=\\ln(1+\\frac{1}{x})\\\\ 并不是很**美观**，现让**对数**的**左右括号**自动**匹配**内容

```tex
f(x)=\ln\left(1+\frac{1}{x}\right)\\
```

f(x)\=ln⁡(1+1x)f(x)=\\ln\\bbox\[#FAA,5px,border:1px\]{\\left(1+\\frac{1}{x}\\right)}\\\\看起来**舒服**多了。当然，**对齐元素**也可使用**占位符**`.` ，例如

```tex
\int_{a}^{b}{\frac{f'(x)}{g(x)}\ \mathrm{d}x}=
\left.\frac{f(x)}{g(x)}\ \right|_a^b+
\int_{a}^{b}\frac{f(x)g'(x)}{g^2(x)}\mathrm{d}x\\
```

∫abf′(x)g(x) dx\=f(x)g(x) |ab+∫abf(x)g′(x)g2(x)dx\\int\_{a}^{b}{\\frac{f'(x)}{g(x)}\\ \\mathrm{d}x}= \\bbox\[#FAA,5px,border:1px\]{\\left.\\frac{f(x)}{g(x)}\\ \\right|\_a^b}+ \\int\_{a}^{b}\\frac{f(x)g'(x)}{g^2(x)}\\mathrm{d}x\\\\

---

## 上下括弧

```dust
\underbrace{[内容]}_{[下标]}
\overbrace{[内容]}^{[上标]}
```

非常**喜欢**该**功能**，它能**直观地表述涵义**，且可**少写繁冗的说明**，比如

E22mc2−12mc2⏞Em\=12mr˙2⏟Te+m(J22m2r2−GMr−GMJ2m2c2r3)⏟Ve\\overbrace{\\frac{E^2}{2\\color{darkblue}mc^2}-\\frac12\\color{darkblue}mc^2}^{\\color{orange}{E\_m}}= \\underbrace{\\frac 12\\color{darkblue}m\\color{orange}{\\dot r^2}}\_{\\color{red}{T\_{e}}}+ \\underbrace{\\color{darkblue}m\\Big( \\frac{\\color{red}{J^2}}{2\\color{darkblue}{m^2}\\color{orange}{r^2}}- \\frac{GM}{\\color{orange}r}-\\frac{GM\\color{red}{J^2}}{\\color{darkblue}{m^2}c^2\\color{orange}{r^3}}\\Big)}\_{\\color{darkblue}{V\_{e}}} \\\\

==当然也会遇到那种==**==无法对齐==**==的==**==状况==**

==J====[====y====]=========∫====0====r====|====π====x====[== ==ρ====g====h====2====+====2====σ====1====+====y====˙====2== ==]====⏟====F====(====y====˙====,====y====;====x====)====d====x====+====2====π====r====Δ====σ====l====⏟====ϕ====(====l====;====r====)====J[\color{blue}y]= \int_0^r\underbrace{\vphantom{\Bigg|}\pi \color{darkorange}x\Big[\ \rho g\color{orange}h^2+2\color{red}\sigma\sqrt{1+\color{blue}{\dot y}^2}\ \Big]}_{F(\dot y,y;x)}dx+ \underbrace{2\pi \color{orange}r\Delta\color{red}\sigma \color{darkblue}l}_{\phi(l;r)}\\==

==我们只需为其添加一个==**==虚拟高度体==**==即可==

```dust
\underbrace{\vphantom{[虚拟高度]}{[内容]}}_{[下标]}
```

==J====[====y====]=========∫====0====r====|====π====x====[== ==ρ====g====h====2====+====2====σ====1====+====y====˙====2== ==]====⏟====F====(====y====˙====,====y====;====x====)====d====x====+====|====2====π====r====Δ====σ====l====⏟====ϕ====(====l====;====r====)====J[\color{blue}y]= \int_0^r\underbrace{\vphantom{\Bigg|}\pi \color{darkorange}x\Big[\ \rho g\color{orange}h^2+2\color{red}\sigma\sqrt{1+\color{blue}{\dot y}^2}\ \Big]}_{F(\dot y,y;x)}dx+ \underbrace{\vphantom{\Bigg|}2\pi \color{orange}r\Delta\color{red}\sigma \color{darkblue}l}_{\phi(l;r)}\\==

==此处我为==**==后者==**==添加了一个==`==\Bigg====|==` ==的==**==虚拟高度==**==，这样==**==两者==**==便能==**==对齐==**==了==

```taggerscript
J[\color{blue}y]=
\int_0^r
\underbrace{\vphantom{\Bigg|}\pi\color{darkorange}
{
    x\Big[\\rho g\color{orange}h^2+2\color{red}\sigma\sqrt{1+\color{blue}{\dot y}^2}\\Big]}_{F(\dot y,y;x)}dx
}+
\underbrace
{
    \vphantom{\Bigg|}2\pi \color{orange}r\Delta\color{red}\sigma \color{darkblue}l}_{\phi(l;r)
}\\
```

又**或者**

```taggerscript
\cos\sqrt{a^2z+b^2}=
\sum_{m=0}^\infty\frac{(-z)^m}{m!}
\underbrace{\sqrt\frac\pi2\ \cfrac{a^{2m}J_{m-\frac12}(b)}{2^mb^{m-\frac12}}}_{\phi(m)}\\
```

cos⁡a2z+b2\=∑m\=0∞(−z)mm!π2 a2mJm−12(b)2mbm−12⏟ϕ(m)\\bbox\[#FAA,10px,border:1px\] {\\cos\\sqrt{a^2z+b^2}= \\sum\_{m=0}^\\infty \\frac{(-z)^m}{m!} \\underbrace{\\bbox\[#ACF,5px,border:1px\]{\\sqrt\\frac\\pi2\\ \\cfrac{a^{2m}J\_{m-\\frac12}(b)}{2^mb^{m-\\frac12}}}}\_{\\bbox\[#ACF,5px,border:1px\]{\\phi(m)}}}\\\\

简直是**惜字如金**却又**不失严谨**者的**福音**。

---

## 公式对齐

```tex
\begin{aligned}
&[内容1]\\\\
&[内容2]
\end{aligned}\\
```

### 分段取值对齐

```tex
2\sum_{n=1}^\infty\sin2nx=\left\{\begin{aligned}
&\cot x&x\ne k\pi\\\\ 
&\frac{\cot x^-+\cot x^+}{2}=0&x=k\pi
\end{aligned}\right.\\
```

2∑n\=1∞sin⁡2nx\={cot⁡xx≠kπcot⁡x−+cot⁡x+2\=0x\=kπ\\bbox\[#ACF,20px,border:1px\]{ 2\\sum\_{n=1}^\\infty\\sin2nx=\\left\\{\\begin{aligned} &\\cot x&x\\ne k\\pi\\\\\\\\ &\\frac{\\cot x^-+\\cot x^+}{2}=0&x=k\\pi \\end{aligned}\\right.}\\\\

此处使用了**自动左括弧高度** (**右对齐元素**使用**占位符**`.`**)**

> 注意`{` 和`}` 属于`Latex` 的**特殊符号**，要显示**该符号**需在其前面加上**转义符**，如`\{` 和`\}` 。

### 等号对齐

```tex
\begin{aligned}
[公式1]=&\
[公式2]\\\\=&\
[公式3]\\\\=&\
[公式4]
\end{aligned}\\
```

例如

```tex
\begin{aligned}
\psi(s)=&\
-\gamma+\sum_{n=0}^\infty\left(\int_0^1 t^{n}\mathrm{d}t- \int_0^1 t^{n+s-1}\mathrm{d}t\right)\\\\=&\
-\gamma+\sum_{n=0}^\infty \int_0^1 t^n(1-t^{s-1})dt\\\\=&\
-\gamma+\int_0^1(1-t^{s-1})\left(\sum_{n=0}^\infty t^n\right)dt\\\\=&\
-\gamma+\int_0^1\frac{1-t^{s-1}}{1-t}\ \mathrm{d}t
\end{aligned}\\
```

ψ(s)\= −γ+∑n\=0∞(∫01tndt−∫01tn+s−1dt)\= −γ+∑n\=0∞∫01tn(1−ts−1)dt\= −γ+∫01(1−ts−1)(∑n\=0∞tn)dt\= −γ+∫011−ts−11−t dt\\bbox\[#FAA,20px,border:1px\]{\\begin{aligned} \\psi(s)=&\\ -\\gamma+\\sum\_{n=0}^\\infty\\left(\\int\_0^1 t^{n}\\mathrm{d}t- \\int\_0^1 t^{n+s-1}\\mathrm{d}t\\right)\\\\\\\\=&\\ -\\gamma+\\sum\_{n=0}^\\infty \\int\_0^1 t^n(1-t^{s-1})dt\\\\\\\\=&\\ -\\gamma+\\int\_0^1(1-t^{s-1})\\left(\\sum\_{n=0}^\\infty t^n\\right)dt\\\\\\\\=&\\ -\\gamma+\\int\_0^1\\frac{1-t^{s-1}}{1-t}\\ \\mathrm{d}t \\end{aligned}}\\\\

其中`=&\` 代表要**对齐**的**第一个等号**，而其最后的`\` 是为了让**公式**更**美观**。

> 而**笔者**常使用`\\\\` 作为**换行**，这样看起来更**舒服**。
> 
> **现在**更倾向于将**较长的公式**分成**几步**去写，让**公式排版**保持**扁平**。

### 阵列对齐

有时将**方程组**摊平，也是不错的**选择**，比如

```tex
\begin{aligned}
&\dot r=\frac{\partial\mathscr H}{\partial p_r}=\frac{p_r}{m}
&\dot \theta=\frac{\partial\mathscr H}{\partial p_\theta}=\frac{p_\theta}{m}\\\\
&\dot p_r=-\frac{\partial\mathscr H}{\partial r}=\frac{p_\theta^2}{2mr^3}-\frac{GMm}{r^2}
&\dot p_\theta=-\frac{\partial\mathscr H}{\partial\theta}=0
\end{aligned}\\
```

r˙\=∂H∂pr\=prmθ˙\=∂H∂pθ\=pθmp˙r\=−∂H∂r\=pθ22mr3−GMmr2p˙θ\=−∂H∂θ\=0\\bbox\[#FEA,20px,border:1px\]{\\begin{aligned} &\\dot r=\\frac{\\partial\\mathscr H}{\\partial p\_r}=\\frac{p\_r}{m} &\\dot \\theta=\\frac{\\partial\\mathscr H}{\\partial p\_\\theta}=\\frac{p\_\\theta}{m}\\\\\\\\ &\\dot p\_r=-\\frac{\\partial\\mathscr H}{\\partial r}=\\frac{p\_\\theta^2}{2mr^3}-\\frac{GMm}{r^2} &\\dot p\_\\theta=-\\frac{\\partial\\mathscr H}{\\partial\\theta}=0 \\end{aligned}}\\\\

这也是**[矩阵](https://zhida.zhihu.com/search?q=%E7%9F%A9%E9%98%B5&zhida%5Fsource=entity&is%5Fpreview=1)**的**对齐方式**，比如**施瓦西度规**

```tex
g_{\mu\nu}=\begin{pmatrix}
-\Bigg(c^2-\frac{2GM}{r}\Bigg)&0&&0&&0\\\\
0&\Bigg(1-\frac{2GM}{r}\Bigg)^{-1}&&0&&0\\\\
0&0&&r^2&&0\\\\
0&0&&0&&r^2\sin^2\theta\
\end{pmatrix}\\
```

gμν\=(−(c2−2GMr)0000(1−2GMr)−10000r20000r2sin2⁡θ )\\small g\_{\\mu\\nu}=\\begin{pmatrix} -\\Bigg(c^2-\\frac{2GM}{r}\\Bigg)&0&&0&&0\\\\\\\\ 0&\\Bigg(1-\\frac{2GM}{r}\\Bigg)^{-1}&&0&&0\\\\\\\\ 0&0&&r^2&&0\\\\\\\\ 0&0&&0&&r^2\\sin^2\\theta\\ \\end{pmatrix}\\\\ 

这里使用了`Latex` 中的**矩阵对齐格式**

```tex
\begin{pmatrix}
[元素00]&[元素01]\\\\
[元素10]&[元素11]
\end{pmatrix}
```

并且强制使用了**增大符号** `\Bigg` (而未使用**符号对齐**) ，当然是期望**括号**能更为**显著**

```tex
\Big(1-\frac{2GM}{r}\Big)^{-1}\\
```

(1−2GMr)−1\\Big(1-\\frac{2GM}{r}\\Big)^{-1}\\\\

```tex
\Bigg(1-\frac{2GM}{r}\Bigg)^{-1}\\
```

(1−2GMr)−1\\bbox\[#AFA,10px,border:1px\]{\\Bigg(1-\\frac{2GM}{r}\\Bigg)^{-1}}\\\\

---

## 字体

### [花体字](https://zhida.zhihu.com/search?q=%E8%8A%B1%E4%BD%93%E5%AD%97&zhida%5Fsource=entity&is%5Fpreview=1)

(1) 在输入**傅里叶变换**、**[拉普拉斯变换](https://zhida.zhihu.com/search?q=%E6%8B%89%E6%99%AE%E6%8B%89%E6%96%AF%E5%8F%98%E6%8D%A2&zhida%5Fsource=entity&is%5Fpreview=1)**和**梅林变换符号**时，最好使用**花体字**。

F{f(t)}(ω)L{f(t)}(s)M{f(t)}(s)\\bbox\[#CAF,10px,border:1px\]{\\mathcal{F}\\Big\\{{f(t)}\\Big\\}(\\omega)}\\quad\\quad \\bbox\[#FAA,10px,border:1px\]{\\mathcal{L}\\Big\\{{f(t)}\\Big\\}(s)}\\quad\\quad \\bbox\[#FEA,10px,border:1px\]{\\mathcal{M}\\Big\\{{f(t)}\\Big\\}(s)}\\\\

**拉普拉斯变换**

```tex
\mathcal L\Big\{\sin b\sqrt x\ \Big\}(a)=
\int_{0}^{\infty}{e^{-ax}\sin b\sqrt x\ dx}=
\frac{b}{2a}\sqrt{\frac{\pi}{a}}\ e^{-\frac{b^2}{4a}}\\
```

L{sin⁡bx }(a)\=∫0∞e−axsin⁡bx dx\=b2aπa e−b24a\\bbox\[#ACF,20px,border:1px\]{\\mathcal L\\Big\\{\\sin b\\sqrt x\\ \\Big\\}(a)= \\int\_{0}^{\\infty}{e^{-ax}\\sin b\\sqrt x\\ dx}= \\frac{b}{2a}\\sqrt{\\frac{\\pi}{a}}\\ e^{-\\frac{b^2}{4a}}}\\\\

(2) 对于表述**函数的阶**的大 OO **字母**，也推荐使用**花体字**，比如

```tex
|\zeta(1-s)|=
\mathcal{O}\left(\sigma^{\sigma-\frac12}e^{-\sigma}\right)\quad
\mathrm{as}\quad\sigma\to\infty\\
```

|ζ(1−s)|\=O(σσ−12e−σ)asσ→∞\\bbox\[#DBF,20px,border:1px\] { |\\zeta(1-s)|= \\mathcal O\\left(\\sigma^{\\sigma-\\frac12}e^{-\\sigma}\\right)\\quad \\mathrm{as}\\quad\\sigma\\to\\infty }\\\\

### 正体字

我们**时常**会遇到一些在 `Latex` 中**尚未存在**的**数学名称**，比如**反双曲正切**

arctanh(x)\\bbox\[#FAA,20px,border:1px\]{arctanh(x)}\\\\可用`\mathrm` **创造**该**函数名**的**正体形式**

arctanh x\\bbox\[#ACF,20px,border:1px\]{\\mathrm{arctanh}\\ x}\\\\当然还可创造它的**简写形式**

th−1x\\bbox\[#ACF,15px,border:1px\]{\\quad\\mathrm{th}^{-1}x\\quad}\\\\ 我用得**最多**的，无非就是书写**留数符号**的时候

```tex
\underset{z=z_k}{\mathrm{Res}}\ 
```

12πi∮Γf(z)dz\=∑k\=1nResz\=zk f(z)\\bbox\[#CAF,20px,border:1px\]{ \\frac1{2\\pi i}\\oint\_{\\Gamma}f(z)\\mathrm{d}z= \\sum\_{k=1}^{n}\\underset{z=z\_k}{\\mathrm{Res}}\\ f(z) }\\\\

如此**书写**该**符号**，会显得更为**生动贴切**。

此处用到了**下标符号**

当然也有**上标符号**

也可用`\raise` 和 `\mathop`**替代**，比如你可以创建**高斯**的**连分数符号**

```clojure
{\raise{-1ex}\mathop{\huge\mathrm{K}}_{n=1}^\infty}
```

Kn\=1∞⁡anbn\=a1b1+a2b2+a3b3+a4b4+⋱\\bbox\[#ACF,10px,border:1px\]{\\raise{-1ex}\\mathop{\\huge\\mathrm{K}}\_{n=1}^\\infty \\frac{a\_n}{b\_n}}= \\bbox\[#FAA,20px,border:1px\]{ \\dfrac{a\_1}{b\_1+\\dfrac{a\_2}{b\_2+\\dfrac{a\_3}{b\_3+\\dfrac{a\_4}{b\_4+\\ddots}}}}}\\\\

```tex
{\raise{-1ex}\mathop{\huge\mathrm{K}}_{n=1}^\infty}\frac{a_n}{b_n}=
\dfrac{a_1}{b_1+\dfrac{a_2}{b_2+\dfrac{a_3}{b_3+\dfrac{a_4}{b_4+\ddots}}}}\\
```

如果**有一天晚上**，你也作了个**梦**

∫0∞exp⁡(−n∫0ϕdθ1−xsin2⁡θ)dϕ\=(n+Kk\=1∞k2x(−)k+1−12n)−1\\bbox\[#CAF,20px,border:1px\]{\\int\_0^\\infty\\exp\\left(-n\\int\_0^\\phi\\frac{d\\theta}{\\sqrt{1-x\\sin^2\\theta}}\\right)d\\phi= \\left(n+{\\raise{-1ex}\\mathop{\\huge\\mathrm{K}}\_{k=1}^\\infty}\\frac{k^2x^{\\frac{(-)^{k+1}-1}{2}}}{n}\\right)^{-1}}\\\\别忘了**告诉我**。

---

## 润色

### 设置字体颜色

从**色彩美学**而言，画面不要超过**三种**色相迥异的**色彩**，而笔者更偏好**蓝**、**红**、**橙**

LLL\\large\\color{blue}{\\mathcal{L}}\\quad\\quad\\quad\\quad \\color{red}{\\mathcal{L}}\\quad\\quad\\quad\\quad \\color{orange}{\\mathcal{L}}\\\\

```tex
\color{blue}
\color{red}
\color{orange}
```

**冷暖协调**，那**灵动**的**温度**跃然于纸上

ds2\=−c2(1−rsr)dt2+(1−rsr)−1dr2+r2dθ2+r2sin2⁡θdφ2ds^2=-c^2\\Big(1-\\frac{\\color{red}{r\_s}}{\\color{orange}r}\\Big)d\\color{purple}t^2+\\Big(1-\\frac{\\color{red}{r\_s}}{\\color{orange}r}\\Big)^{-1}d\\color{orange}r^2+\\color{orange}r^2d\\color{blue}\\theta^2+\\color{orange}r^2\\sin^2\\color{blue}\\theta d\\varphi^2\\\\

尤其是对于**张量指标**的**书写**，仅通过**颜色**，我们便能一眼**知晓**哪些**指标**需**缩并**，哪些**指标**要**求和**

duρds+12gλρ(∂μgλν+∂νgλμ−∂λgμν)uμuν\=0\\frac{du^\\color{red}\\rho}{ds}+ \\frac12g^{\\color{orange}\\lambda\\color{red}\\rho}(\\partial\_\\color{red}\\mu g\_{\\color{orange}\\lambda\\color{blue}\\nu}+\\partial\_\\color{blue}\\nu g\_{\\color{orange}\\lambda\\color{red}\\mu}-\\partial\_\\color{orange}\\lambda g\_{\\color{red}\\mu\\color{blue}\\nu}) u^\\color{red}\\mu u^\\color{blue}\\nu =0\\\\

### 背景色

```inform7
\bbox[#[颜色代码],[颜色框大小]px,border:[边框粗细]px]
```

如今**笔者**更**偏爱**为**心仪**的**公式**搭配**背景**

∫0πsin2⁡x ln⁡sin⁡x dx\=π4(1−2ln⁡2)\\bbox\[#CBF,20px,border:1px\] {\\int\_0^\\pi \\sin^2x\\ \\ln\\sin x\\ dx= \\frac{\\pi}{4}\\Big(1-2\\ln2\\Big)} \\\\

一般的**可选颜色**代码为

```1c
黄色 #FEA
红色 #FAA
绿色 #AFA
蓝色 #ACF
紫色 #CAF
```

**蓝色**为**主色调**，`20` **像素**也是一个**合适的尺寸**，因此可给出**默认边框代码**

```angelscript
\bbox[#ACF,20px,border:1px]
```

比如**默认**它是这样的

∫0πp(x)ln⁡sin⁡x dx\=−ln⁡2∫0πp(x)dx−i2∫0πp(x)(2x−π)dx+πc\\bbox\[#ACF,20px,border:1px\] {\\int\_0^\\pi p(x)\\ln\\sin x\\ dx= -\\ln2\\int\_0^\\pi p(x)dx- \\frac i2\\int\_0^\\pi p(x)(2x-\\pi)dx+ \\pi c} \\\\

若你有一个**内容丰富**的**公式版面**，也许可以这么做

∫ ⋅→F(z)dz\=−2πi∫−a+af(x−ia)e2π(a+ix)−1 dx∫ ⋅ ↑F(z)dz\=−2π∫−a+af(a+ix)e−2π(x−ia)−1 dx∫ ⋅←F(z)dz\=2πi∫−a+af(x+ia)e−2π(a−ix)−1 dx∫ ↓⋅F(z)dz\=2π∫−a+af(−a+ix)e−2π(x+ia)−1 dx\\bbox\[#FFA,20px,border:1px\] {\\quad \\begin{aligned} &\\int\_{\\ \\underset{\\rightarrow}{\\cdot}}F(z)dz= -2\\pi i\\int\_{-a}^{+a}\\frac{f(x-ia)}{e^{2\\pi(a+i x)}-1}\\ dx\\\\\\\\\\\\ &\\int\_{\\ \\cdot\\ \\uparrow}F(z)dz= -2\\pi\\int\_{-a}^{+a}\\frac{f(a+ix)}{e^{-2\\pi(x-ia)}-1}\\ dx\\\\\\\\\\\\ &\\int\_{\\ \\overset{\\leftarrow}{\\cdot}}F(z)dz= 2\\pi i\\int\_{-a}^{+a}\\frac{f(x+ia)}{e^{-2\\pi(a-ix)}-1}\\ dx\\\\\\\\\\\\ &\\int\_{\\ \\downarrow\\cdot}F(z)dz= 2\\pi\\int\_{-a}^{+a}\\frac{f(-a+ix)}{e^{-2\\pi(x+ia)}-1}\\ dx \\end{aligned} \\quad}\\\\

**边框**还可以**嵌套**

∫π2xdxsin⁡x⏟ln⁡|tan⁡x2|\=−ln⁡|cot⁡x2|\=2∑n\=1∞∫π2xsin⁡(2n−1)x dx\\bbox\[#FAA,10px,border:1px\] {\\underbrace{ \\bbox\[#ACF,15px,border:1px\]{\\int\_{\\frac\\pi2}^x\\frac{dx}{\\sin x}} }\_{ \\bbox\[#ACF,10px,border:1px\]{\\ln\\left|\\tan\\frac x2\\right|=-\\ln\\left|\\cot\\frac x2\\right|} }=2\\sum\_{n=1}^\\infty\\int\_{\\frac\\pi2}^x\\sin(2n-1)x\\ dx}\\\\

---

当你**掌握**了以上**所有技巧**，那么**数学**就可**真正**称得上是一幅**艺术画作**了

−12πi∫ ⋅→F(z)dz\=a\=N+12∫−(N+12)+(N+12)f(x−iN−i2)eπ(2N+1)⏟∞ as N→∞ ei2πx−1 dx12πi∫ ⋅←F(z) dz\=a\=N+12∫−(N+12)+(N+12)f(x+iN+i2)e−π(2N+1)⏟0 as N→∞ e−i2πx−1 dx −12π∫ ⋅ ↑F(z) dz\=a\=N+12∫−(N+12)+(N+12)f(N+12+ix)e−2πxei2πNeiπ⏟−1−1 dx12π∫ ↓⋅F(z) dz\=a\=N+12∫−(N+12)+(N+12)f(−N−12+ix)e−2πxe−i2πNe−iπ⏟−1−1 dx\\small\\begin{aligned} &\\bbox\[#FEA,20px,border:1px\]{-\\frac1{2\\pi i} \\int\_{\\ \\underset{\\rightarrow}{\\cdot}}F(z)dz\\xlongequal{a=N+\\frac12} \\int\_{-(N+\\frac12)}^{+(N+\\frac12)}\\frac{f(x-iN-\\frac i2)} {\\underbrace{\\bbox\[#ACF,10px,border:1px\]{e^{\\pi(2N+1)}}}\_ {\\bbox\[#ACF,5px,border:1px\]{\\infty\\ \\mathrm{as}\\ N\\to\\infty}}\\ e^{i 2\\pi x}-1}\\ \\mathrm{d}x\\quad\\quad}\\\\\\\\ &\\bbox\[#FAA,20px,border:1px\]{\\quad\\frac1{2\\pi i} \\int\_{\\ \\overset{\\leftarrow}{\\cdot}}F(z)\\ \\mathrm{d}z\\xlongequal{a=N+\\frac12} \\int\_{-(N+\\frac12)}^{+(N+\\frac12)}\\frac{f(x+iN+\\frac i2)}{ {\\underbrace{\\bbox\[#ACF,10px,border:1px\]{e^{-\\pi(2N+1)}}}\_ {\\bbox\[#ACF,5px,border:1px\]{0\\ \\mathrm{as}\\ N\\to\\infty}}}\\ e^{-i2\\pi x}-1}\\ \\mathrm{d}x\\space\\space}\\\\\\\\ &\\bbox\[#CAF,20px,border:1px\]{-\\frac1{2\\pi} \\int\_{\\ \\cdot\\ \\uparrow}F(z)\\ \\mathrm{d}z\\xlongequal{a=N+\\frac12} \\int\_{-(N+\\frac12)}^{+(N+\\frac12)}\\frac{f(N+\\frac12+ix)}{e^{-2\\pi x} \\underbrace{\\bbox\[#ACF,10px,border:1px\]{e^{i2\\pi N}e^{i\\pi}}}\_ {\\bbox\[#ACF,5px,border:1px\]{-1}} -1}\\ \\mathrm{d}x\\quad\\quad}\\\\\\\\ &\\bbox\[#ABF,20px,border:1px\]{\\quad\\frac1{2\\pi} \\int\_{\\ \\downarrow\\cdot}F(z)\\ \\mathrm{d}z\\xlongequal{a=N+\\frac12} \\int\_{-(N+\\frac12)}^{+(N+\\frac12)}\\frac{f\\left(-N-\\frac12+ix\\right)}{e^{-2\\pi x} \\underbrace{\\bbox\[#ACF,10px,border:1px\]{e^{-i2\\pi N}e^{-i\\pi}}}\_ {\\bbox\[#ACF,5px,border:1px\]{-1}} -1}\\ \\mathrm{d}x\\quad} \\end{aligned}\\\\

```tex
\small\begin{aligned}

&\bbox[#FEA,20px,border:1px]{-\frac1{2\pi i}
\int_{\ \underset{\rightarrow}{\cdot}}F(z)dz\xlongequal{a=N+\frac12}
\int_{-(N+\frac12)}^{+(N+\frac12)}\frac{f(x-iN-\frac i2)}
{\underbrace{\bbox[#ACF,10px,border:1px]{e^{\pi(2N+1)}}}_
{\bbox[#ACF,5px,border:1px]{\infty\ \mathrm{as}\ N\to\infty}}\ e^{i 2\pi x}-1}\ \mathrm{d}x\quad\quad}\\\\

&\bbox[#FAA,20px,border:1px]{\quad\frac1{2\pi i}
\int_{\ \overset{\leftarrow}{\cdot}}F(z)\ \mathrm{d}z\xlongequal{a=N+\frac12} 
\int_{-(N+\frac12)}^{+(N+\frac12)}\frac{f(x+iN+\frac i2)}{ 
{\underbrace{\bbox[#ACF,10px,border:1px]{e^{-\pi(2N+1)}}}_
{\bbox[#ACF,5px,border:1px]{0\ \mathrm{as}\ N\to\infty}}}\ e^{-i2\pi x}-1}\ \mathrm{d}x\space\space}\\\\

&\bbox[#CAF,20px,border:1px]{-\frac1{2\pi}
\int_{\ \cdot\ \uparrow}F(z)\ \mathrm{d}z\xlongequal{a=N+\frac12} 
\int_{-(N+\frac12)}^{+(N+\frac12)}\frac{f(N+\frac12+ix)}{e^{-2\pi x}
\underbrace{\bbox[#ACF,10px,border:1px]{e^{i2\pi N}e^{i\pi}}}_
{\bbox[#ACF,5px,border:1px]{-1}} -1}\ \mathrm{d}x\quad\quad}\\\\

&\bbox[#ABF,20px,border:1px]{\quad\frac1{2\pi}
\int_{\ \downarrow\cdot}F(z)\ \mathrm{d}z\xlongequal{a=N+\frac12}
\int_{-(N+\frac12)}^{+(N+\frac12)}\frac{f\left(-N-\frac12+ix\right)}{e^{-2\pi x}
\underbrace{\bbox[#ACF,10px,border:1px]{e^{-i2\pi N}e^{-i\pi}}}_
{\bbox[#ACF,5px,border:1px]{-1}} -1}\ \mathrm{d}x\quad}

\end{aligned}\\
```

---

