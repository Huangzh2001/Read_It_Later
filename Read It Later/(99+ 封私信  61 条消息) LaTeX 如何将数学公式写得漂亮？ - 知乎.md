---
date: 2025-03-12T14:00:10+08:00
url: https://www.zhihu.com/question/29816700/answer/2307586513
Readed: true
---
[LaTeX](https://www.zhihu.com/topic/19568710)

[

数学公式

](https://www.zhihu.com/topic/19581831)

[

写作技巧

](https://www.zhihu.com/topic/19676958)

[

LaTeX 排版与设计

](https://www.zhihu.com/topic/19773080)

被浏览

**159,922**

[查看全部 13 个回答](https://www.zhihu.com/question/29816700)

153 人赞同了该回答

Hi 大家好，我是Realcat，今天给大家分享一个工具。

@sibinmohan 前两天在[Github](https://zhida.zhihu.com/search?content_id=449643055&content_type=Answer&match_order=1&q=Github&zhida_source=entity)上开源了一款”神器“，它能够**给[Latex](https://zhida.zhihu.com/search?content_id=449643055&content_type=Answer&match_order=1&q=Latex&zhida_source=entity)公式添加漂亮的注释，极大地增加了数学公式的可读性与理解性**，短短两天获得659个star，各位写论文的同学们用起来！

项目：

[github.com/synercys/annotated\_latex\_equations​github.com/synercys/annotated\_latex\_equations](https://link.zhihu.com/?target=http%3A//github.com/synercys/annotated_latex_equations)

![](https://pica.zhimg.com/80/v2-42f17cdeaf9f75ee85e1c40101700f73_1440w.webp?source=2c26e567)

效果图如下：

![](https://picx.zhimg.com/80/v2-8e1b3aa1c0a71f51ffc5d9030e7feb0c_1440w.webp?source=2c26e567)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='1080'%20height='547'%3E%3C/svg%3E)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='1080'%20height='527'%3E%3C/svg%3E)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='1080'%20height='421'%3E%3C/svg%3E)

众网友直呼有用，再也不用读文字理解公式了...

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='583'%20height='158'%3E%3C/svg%3E)

网友提到，“我也为幻灯片做过类似的工作，但在论文中并没有尝试”

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='579'%20height='430'%3E%3C/svg%3E)

这位网友提到“原来曾经用手工注释的方式添加标注，现在有这个工具了，感觉666”

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='585'%20height='604'%3E%3C/svg%3E)

**关于作者**

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='1080'%20height='720'%3E%3C/svg%3E)

Prof. Sibin Mohan

作者是来自[俄勒冈州立大学](https://zhida.zhihu.com/search?content_id=449643055&content_type=Answer&match_order=1&q=%E4%BF%84%E5%8B%92%E5%86%88%E5%B7%9E%E7%AB%8B%E5%A4%A7%E5%AD%A6&zhida_source=entity)电子工程和计算机科学学院的副教授 Prof. Sibin Mohan。他还在伊利诺伊大学厄巴纳-香槟分校计算机科学系担任兼职教师。

Sibin 的研究兴趣是系统、安全、网络和自主系统领域。目前的研究工作包括[CPS](https://zhida.zhihu.com/search?content_id=449643055&content_type=Answer&match_order=1&q=CPS&zhida_source=entity)的弹性和安全性，自主和物联网式的系统，安全云计算，使用软件定义网络（[SDN](https://zhida.zhihu.com/search?content_id=449643055&content_type=Answer&match_order=1&q=SDN&zhida_source=entity)）的弹性安全关键系统，[V2X系统](https://zhida.zhihu.com/search?content_id=449643055&content_type=Answer&match_order=1&q=V2X%E7%B3%BB%E7%BB%9F&zhida_source=entity)的安全性和理解无人机群的行为。

主页：

[编辑于 2022-01-12 13:14](https://www.zhihu.com/question/29816700/answer/2307586513)

#### 更多回答

一、

现在只能想起一点，方程组不要用 eqnarray，而要用 align。

然后说一下原因。

前者要用 …&…&… 对齐，问题是对齐的位置空格会偏大；

后者用 …&… 对齐，没有前者的问题，很自然。

二、多用用已经存在的、针对性强的 package。

比如 mathtools, braket, 还有一个专门以国际单位制写数据和单位的包（具体名字现在不记得。单位也不是乱写的，比如按照标准，数字和单位之间不是紧挨而是需要一个空格；单位符号应该用正体而不是斜体等等）

三、几个常用的特殊符号∶自然对数的底 e，微分符号 d，虚数单位 i，个人建议是都用正体，不用斜体。比如自定义命令 \\me 为 \\mathrm{e}

关于这一点，其实至少满足如下“原则”：同一个公式中，不同符号和不同意义一一对应，避免歧义。

比如一个公式中既有求和指标 i，又有虚数单位；既有元电荷又有 e 指数；既有距离 d，又有微分，分别用相同的符号表示，是不合适的。

另一个关于斜体正体的“原则”：表示变量的符号斜体，表示文本或文本缩写的符号用正体。（这个和各种函数名是正体是相一致的：比如 sin, cos 是正体，它们都可以看成是 sine, cosine 的文本缩写；同时这也是我说 e, d, i 要用正体的原因，比如 i 可以看作 imaginary 的缩写。至少它们都不是变量。）

四、个人觉得，行内高度会压缩的分数 \\frac 不太好看，一般用 \\dfrac 替换

从大一寒假开始用 \\LaTeX 记笔记有一段时间了，眼看手边的笔记越堆越多，积攒了一些数学公式常用的命令，在此发送一个尚不完善的版本，以后有新内容或许会再更新。

对于刚走出新手村的我来说，各种各样的环境真多，实现的效果既有相似又有不同。

要记住真费工夫，所以把用过的实用的操作记录下来，以供下次查找，并不断完善是不二之选。

各种命令的来源有刘海洋老师的《 \\LaTeX 入门》、知乎、CSDN、网站 \\LaTeX 编辑部等，还有一份80页左右名叫《The \\LaTeX Mathematics Companion》（Helin Gai-Duke University）专门讲数学公式的书。

编译器只用过TeXstudio，还有在线编译器overleaf，两种都强推，尤其是overleaf，既不需要安装软件，又支持多人共同编辑，要做的就只是注册一个账号，其他的操作都与其他编译器无异，对于参加建模竞赛的小伙伴绝对是一大利器。

废话就说这么多，下面是用 \\LaTeX 收集的常用的数学公式排版的记录，先给出例子，再用抄录环境给出代码实现，按照输出效果，尝试自己是否能够输出例子中给出的数学公式，再比较自己的输出和给出的例子哪里不同，不同的原因是什么，思考是否可以通过其他代码实现相同或者不同的效果。

想要熟练掌握数学公式的输出，最好的方式是多尝试，可以找一本有公式的教科书，选取书中的例子来尝试自己能否输出相同的效果，比如《高等数学》（各种“形式”的公式比较全面，矩阵、分式、多项式、多行公式、分段函数都有），或者任何能找到各种数学公式的资源。

顺带提一下常用的数学宏包，最广为人知的就是amsmath宏包，其定义了多行公式环境和一系列数学公式命令，如\\cfrac可以实现更美观的分式排版。笔者还会用到两个宏包，amsfonts宏包和bm宏包，前者提供各种数学符号字体，后者提供数学符号加粗命令\\bm，其实现的效果较\\textbf命令更为美观。

| 常用数学宏包 | 实现效果 |
| --- | --- |
| amsmath | 多行公式环境和一系列命令，满足绝大多数需求 |
| amsfonts | 各种数学符号的字体 |
| bm | 数学符号加粗命令\\bm |

各种希腊字母虽然在下面也有汇总，但先单独罗列在此，以方便读者的查取。以前不知道有些希腊字母命令前面加上\\var可能会有不同的效果。下面命令的实际效果请以 \\LaTeX 编译器中的效果为主，不知知乎公式的输出是否有所不同。以下也许并非全是希腊字母，或许称为数学符号比较合适。笔者发现TeXstudio中不支持一些以下命令，而知乎公式编辑支持，可能是没引入合适宏包的缘故。

\\alpha \\alpha \\beta \\beta \\gamma \\gamma \\delta \\delta \\epsilon \\epsilon \\zeta \\zeta \\eta \\eta

\\theta \\theta \\iota \\iota \\kappa \\kappa \\lambda \\lambda \\mu \\mu \\nu \\nu \\xi \\xi

\\omicron \\omicron \\Pi \\Pi \\rho \\rho \\sigma \\sigma \\Sigma \\Sigma \\varDelta \\varDelta \\tau \\tau

\\Tau \\tau \\upsilon \\upsilon \\Upsilon \\Upsilon \\phi \\phi \\Phi \\Phi \\varphi \\varphi \\chi \\chi

\\psi \\psi \\Psi \\Psi \\Gamma \\Gamma \\Delta \\Delta \\Theta \\Theta \\Lambda \\Lambda \\varGamma \\varGamma

\\varOmega \\varOmega \\varPi \\varPi \\varTheta \\varTheta \\varUpsilon \\varUpsilon

以上的排版未按照字母顺序，是考虑到一些数学符号仅仅是在之前加上了var，同时待加入完善所有的数学符号。

数学符号的各种字体命令也罗列在此。

X(original)

\\textbf{X} \\textbf{X} \\bm{X} \\bm{X} \\mathbf{X} \\mathbf{X} \\mathsf{X} \\mathsf{X}

\\mathit{X} \\mathit{X} \\mathcal{X} \\mathcal{X} \\mathbb{X} \\mathbb{X} \\mathfrak{X} \\mathfrak{X}

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='947'%20height='481'%3E%3C/svg%3E)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='859'%20height='1178'%3E%3C/svg%3E)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='805'%20height='1183'%3E%3C/svg%3E)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='826'%20height='1165'%3E%3C/svg%3E)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='802'%20height='1170'%3E%3C/svg%3E)

![](https://www.zhihu.com/question/29816700/answer/www.w3.org/2000/svg'%20width='804'%20height='679'%3E%3C/svg%3E)

以上就是目前收录的常用数学命令，或许还会更新。我也只是个新手小白，多关注 \\LaTeX 的数学公式排版，对于其他方面入图表等，能做的只是基本会用。希望能和更多的 \\LaTeX 用户交流，如果您有想要实现但不能的数学公式，可以不吝发给我，我还挺闲的~

```text
%\begin{设置文本类型、引入宏包}
\documentclass[12pt,a4paper]{ctexart}%文本类型，文本类型为中文文章
\usepackage[utf8]{inputenc}%所使用的宏包
\usepackage[T1]{fontenc}
\usepackage{amsmath}%常用的数学宏包
\usepackage{amssymb}
\usepackage{graphicx}
\usepackage{float}
\RequirePackage{caption}
\usepackage{subfigure}
\usepackage{fancyhdr}
\usepackage{listings}
\usepackage{makecell}%表格内换行的宏包
\usepackage{diagbox}
\usepackage{listings}
\usepackage[colorlinks, linkcolor=black, anchorcolor=blue, citecolor=black]{hyperref}
\usepackage{tikz}
\usepackage{pxfonts}
\usepackage{geometry}
\usepackage{setspace}
%\usepackage{mathrsfs}%数学字体宏包
\usepackage{amsfonts}%数学字体宏包
\usepackage{bm}%数学符号加粗
\usepackage{comment}%批量注释的宏包
%\end{设置文本类型、引入宏包}

%\begin{设置页面尺寸}
\setstretch{1} 
\geometry{a4paper,left=25mm,right=25mm,top=25mm,bottom=25mm}
%\end{设置页面尺寸}

%字号的设置用\zihao{*} 其中*为数字，-4为小四，4为四号，3为三号
%字体的设置用	{\songti 宋体}、{\heiti 黑体}、{\fangsong 仿宋}、{\kaishu 楷书}，使用时把字加在花括号内如{\songti 同济大学}
%不使用上述代码时默认宋体小四

%\begin{抄录代码环境lstlisting的设置}，不需要comment环境注释掉即可
\usepackage{listings}
\usepackage{color}

\definecolor{dkgreen}{rgb}{0,0.6,0}
\definecolor{gray}{rgb}{0.5,0.5,0.5}
\definecolor{mauve}{rgb}{0.58,0,0.82}

\lstset{frame=tb,
	language=Python,
	aboveskip=3mm,
	belowskip=3mm,
	showstringspaces=false,
	columns=flexible,
	basicstyle={\small\ttfamily},
	numbers=none,
	numberstyle=\tiny\color{gray},
	keywordstyle=\color{blue},
	commentstyle=\color{dkgreen},
	stringstyle=\color{mauve},
	breaklines=true,
	breakatwhitespace=true,
	tabsize=3
}
%\end{抄录代码环境lstlisting的设置}

%\begin{页眉页脚设置}
\pagestyle{fancy}
\fancyhf{} %清除原页眉页脚样式
\renewcommand{\headrulewidth}{0mm} % 设置页眉页脚横线及样式 %页眉线宽，设为0可以去页眉线
\renewcommand{\footrulewidth}{0mm} %页脚线宽，设为0可以去页眉线
\cfoot{\thepage} 
%\end{页眉页脚设置}

%\begin{正文开始}
\begin{document}

\section{\zihao{4} {\heiti latex}}
\begin{lstlisting}
\noindent%取消段首缩进
\end{lstlisting}
\noindent 分段函数

\noindent 表示分段函数的环境有三种，分别是aligned、array、cases环境。

\noindent $ f(x)=\left\{
\begin{aligned}
x & =  \cos(t) \\
y & =  \sin(t) \\
z & =  \frac xy
\end{aligned}
\right.$
\begin{lstlisting}
$f(x)=\left\{
\begin{aligned}
x & =  \cos(t) \\
y & =  \sin(t) \\
z & =  \frac xy
\end{aligned}
\right.$
\end{lstlisting}
$F^{HLLC}=\left\{
\begin{array}{rcl}
F_L       &      & {0      <      S_L}\\
F^*_L     &      & {S_L \leq 0 < S_M}\\
F^*_R     &      & {S_M \leq 0 < S_R}\\
F_R       &      & {S_R \leq 0}
\end{array} \right. $
\begin{lstlisting}
$F^{HLLC}=\left\{
\begin{array}{rcl}
F_L       &      & {0      <      S_L}\\
F^*_L     &      & {S_L \leq 0 < S_M}\\
F^*_R     &      & {S_M \leq 0 < S_R}\\
F_R       &      & {S_R \leq 0}
\end{array} \right. $
\end{lstlisting}
$f(x)=
\begin{cases}
0& \text{x=0}\\
1& \text{x!=0}
\end{cases}$
\begin{lstlisting}
$f(x)=
\begin{cases}
0& \text{x=0}\\
1& \text{x!=0}
\end{cases}$
\end{lstlisting}
\noindent 带编号居中的分段函数
\begin{eqnarray}
f(x)=\left\{
\begin{aligned}
x & = & \cos(t) \\
y & = & \sin(t) \\
z & = & \frac xy
\end{aligned}
\right.
\end{eqnarray}
\begin{lstlisting}
\begin{eqnarray}%不需要加上美元符号
f(x)=\left\{
\begin{aligned}
x & = & \cos(t) \\
y & = & \sin(t) \\
z & = & \frac xy
\end{aligned}
\right.
\end{eqnarray}
\end{lstlisting}
\begin{eqnarray}
F^{HLLC}=\left\{
\begin{array}{rcl}
F_L      &     & {0     <     S_L}\\
F^*_L    &     & {S_L \leq 0 < S_M}\\
F^*_R    &     & {S_M \leq 0 < S_R}\\
F_R      &     & {S_R \leq 0}
\end{array} \right.
\end{eqnarray}
\begin{lstlisting}
\begin{eqnarray}
F^{HLLC}=\left\{
\begin{array}{rcl}
F_L      &     & {0     <     S_L}\\
F^*_L    &     & {S_L \leq 0 < S_M}\\
F^*_R    &     & {S_M \leq 0 < S_R}\\
F_R      &     & {S_R \leq 0}
\end{array} \right.
\end{eqnarray}
\end{lstlisting}
\begin{eqnarray}
f(x)=
\begin{cases}
0& x=0 \\
1& x \neq 0
\end{cases}
\end{eqnarray}
\begin{lstlisting}
\begin{eqnarray}
f(x)=
\begin{cases}
0& x=0 \\
1& x \neq 0
\end{cases}
\end{eqnarray}
\end{lstlisting}
\noindent 控制括号的大小

\noindent $\Bigg ( \bigg [ \Big \{ \big \langle \left | \| x \| \right | \big \rangle \Big \} \bigg ] \Bigg )$
\begin{lstlisting}
\Bigg ( \bigg [ \Big \{ \big \langle \left | \| x \| \right | \big \rangle \Big \} \bigg ] \Bigg )
\end{lstlisting}
\noindent 各种括号

\noindent $\left(\cfrac{a}{b}\right)
\left[\cfrac{a}{b}\right]
\left\{\cfrac{a}{b}\right\}
\left\langle \cfrac{a}{b}\right\rangle
\left|\cfrac{a}{b}\right|
\left\|\cfrac{a}{b}\right\|
\left\{\cfrac{a}{b}\right.
\left.\cfrac{a}{b}\right\}$
\begin{lstlisting}
$\left(\cfrac{a}{b}\right)
\left[\cfrac{a}{b}\right]
\left\{\cfrac{a}{b}\right\}
\left\langle \cfrac{a}{b}\right\rangle
\left|\cfrac{a}{b}\right|
\left\|\cfrac{a}{b}\right\|
\left\{\cfrac{a}{b}\right.
\left.\cfrac{a}{b}\right\}$
\end{lstlisting}
\begin{equation}
\delta\times\varepsilon=\theta
\end{equation}
\begin{equation*}
\varphi-\rho\neq\kappa
\end{equation*}
\begin{lstlisting}
\begin{equation}
\delta\times\varepsilon=\theta
\end{equation}
\begin{equation*}
\varphi-\rho\neq\kappa
\end{equation*}
\end{lstlisting}
\noindent $\neq$
\begin{lstlisting}
$\neq$
\end{lstlisting}
$\epsilon$$\varepsilon$
\begin{lstlisting}
$\epsilon$$\varepsilon$
\end{lstlisting}
$\Delta$$\varDelta$
\begin{lstlisting}
$\Delta$$\varDelta$	
\end{lstlisting}
$\phi$$\varphi$
\begin{lstlisting}
$\phi$$\varphi$
\end{lstlisting}
$y_1'$
$y_1''$
\begin{lstlisting}
$y_1'$
$y_1''$
\end{lstlisting}
$\sqrt[n+1]{x+y}$
\begin{lstlisting}
$\sqrt[n+1]{x+y}$	
\end{lstlisting}
\noindent 分式

\noindent$\sqrt[\leftroot{1}\uproot{3}\varphi]{\varDelta}$
\begin{lstlisting}
$\sqrt[\leftroot{1}\uproot{3}\varphi]{\varDelta}$
\end{lstlisting}
$\sqrt[\beta]{k}$
$\sqrt[\leftroot{2}\uproot{4}\delta]{k}$
$\sqrt[\leftroot{1}\uproot{3}\delta]{k}$
\begin{lstlisting}
$\sqrt[\beta]{k}$
$\sqrt[\leftroot{2}\uproot{4}\delta]{k}$
$\sqrt[\leftroot{1}\uproot{3}\delta]{k}$	
\end{lstlisting}
$\sqrt[\leftroot{1}\uproot{3}\varphi]{\mathstrut y}$
\begin{lstlisting}
$\sqrt[\leftroot{1}\uproot{3}\varphi]{\mathstrut y}$
\end{lstlisting}
$y\mathstrut y$
\begin{lstlisting}
$y\mathstrut y$
\end{lstlisting}
$\sqrt{\smash[b]{y}}$
\begin{lstlisting}
$\sqrt{\smash[b]{y}}$
\end{lstlisting}
\begin{equation}
\sqrt{\sqrt{\sqrt{\sqrt{\sqrt{1+x}}}}}
\end{equation}
$\sqrt{\sqrt{\sqrt{\sqrt{\sqrt{1+x}}}}}$

\noindent $\displaystyle{\sqrt{\sqrt{\sqrt{\sqrt{\sqrt{1+x}}}}}}$
\begin{lstlisting}
\begin{equation}
\sqrt{\sqrt{\sqrt{\sqrt{\sqrt{1+x}}}}}
\end{equation}
$\sqrt{\sqrt{\sqrt{\sqrt{\sqrt{1+x}}}}}$
$\displaystyle{\sqrt{\sqrt{\sqrt{\sqrt{\sqrt{1+x}}}}}}$
\end{lstlisting}
\noindent amsmath宏包定义了多行公式环境和一系列数学公式命令，如\textbackslash cfrac命令使分数的排版更加优美。

\noindent bm宏包提供数学符号加粗命令\textbackslash bm。

\noindent $a\bm{a}A\bm{A}b\bm{b}B\bm{B}$
\begin{lstlisting}
$a\bm{a}A\bm{A}b\bm{b}B\bm{B}$
\end{lstlisting}
\noindent amsfonts宏包提供改变数学字体的命令。

\noindent $X\mathbf{X}\mathsf{X}\mathit{X}\mathcal{X}\mathbb{X}\mathfrak{X}$
\begin{lstlisting}
$X\mathbf{X}\mathsf{X}\mathit{X}\mathcal{X}\mathbb{X}\mathfrak{X}$
\end{lstlisting}
\noindent $\sigma\varsigma
\Gamma\varGamma
\Omega\varOmega
\Pi\varPi
\Theta\varTheta
\theta\vartheta$
\begin{lstlisting}
$\sigma\varsigma
\Gamma\varGamma
\Omega\varOmega
\Pi\varPi
\Theta\varTheta
\theta\vartheta$
\end{lstlisting}
\noindent 多行公式

\noindent $\begin{aligned}
\text{磁化物体的矢势：}A&=\cfrac{{\mu}_{0}}{4\pi}\int\cfrac{\vec{M}\times\hat{\eta}}{{\eta}^2}\\
&=\cfrac{{\mu}_{0}}{4\pi}{\int}_{V}\cfrac{{\vec{J}}_{b}}{\eta}d\tau
+\cfrac{{\mu}_{0}}{4\pi}{\oint}_{S}\cfrac{{\vec{K}}_{b}}{\eta}d\sigma
\end{aligned}$
\begin{lstlisting}
$\begin{aligned}
\text{磁化物体的矢势：}A&=\cfrac{{\mu}_{0}}{4\pi}\int\cfrac{\vec{M}\times\hat{\eta}}
{{\eta}^2}\\
&=\cfrac{{\mu}_{0}}{4\pi}{\int}_{V}\cfrac{{\vec{J}}_{b}}{\eta}d\tau
+\cfrac{{\mu}_{0}}{4\pi}{\oint}_{S}\cfrac{{\vec{K}}_{b}}{\eta}d\sigma
\end{aligned}$
\end{lstlisting}
\noindent 希腊字母

\noindent $\alpha\beta\gamma\delta\epsilon\zeta\eta\theta\iota\kappa\lambda\mu\nu\xi\pi\rho\sigma\tau\upsilon\phi\chi\psi\Gamma\Theta\Lambda\Xi\Sigma\varepsilon$
\begin{lstlisting}
$\alpha\beta\gamma\delta\epsilon\zeta\eta\theta\iota\kappa\lambda\mu\nu\xi\pi
\rho\sigma\tau\upsilon\phi\chi\psi\Gamma\Theta\Lambda\Xi\Sigma\varepsilon$
\end{lstlisting}
\noindent $\hat{a}
\widehat{(\bm{a},\bm{b})}
\widetilde{a}
\dot{a}
\ddot{a}
\vec{a}
\bar{a}
\acute{a}
\grave{a}
\breve{a}
\check{a}$
\begin{lstlisting}
$\hat{a}
\widehat{(\bm{a},\bm{b})}
\widetilde{a}
\dot{a}
\ddot{a}
\vec{a}
\bar{a}
\acute{a}
\grave{a}
\breve{a}
\check{a}$
\end{lstlisting}
\noindent $\mathop{A}\limits^{\rightarrow}
\mathop{A}\limits^{\leftarrow}$
\begin{lstlisting}
$\mathop{A}\limits^{\rightarrow}
\mathop{A}\limits^{\leftarrow}$	
\end{lstlisting}
\noindent $\left\{
\begin{array}{lcl}
x=r\sin\varphi\cos\theta,  &     &{0\leq\varphi\leq\pi}\\
y=r\sin\varphi\sin\theta,  &     &{0\leq\theta\leq 2\pi}\\
z=a\cos\varphi             &     &{}\\
\end{array}
\right.$
\begin{lstlisting}
$\left\{
\begin{array}{lcl}
x=r\sin\varphi\cos\theta,  &     &{0\leq\varphi\leq\pi}\\
y=r\sin\varphi\sin\theta,  &     &{0\leq\theta\leq 2\pi}\\
z=a\cos\varphi             &     &{}\\
\end{array}
\right.$
\end{lstlisting}
\noindent array环境后的必选参数用于指定每列的对齐方式。

\noindent $\approx\le\leq\ge\geq\ne\neq\lvertneqq\equiv\not\equiv
\doteq\doteqdot\gneq\lneq\geqq\lneqq\ngeq\nleq\ngeqq\nleqq$
\begin{lstlisting}
$\approx\le\leq\ge\geq\ne\neq\lvertneqq\equiv\not\equiv
\doteq\doteqdot\gneq\lneq\geqq\lneqq\ngeq\nleq\ngeqq\nleqq$
\end{lstlisting}
\noindent $\alpha\beta
\gamma\Gamma\varGamma
\delta\Delta\varDelta
\epsilon\varepsilon
\lambda\Lambda\varLambda
\zeta\eta\iota
\theta\Theta\vartheta\varTheta
\kappa\varkappa
\mu\nu
\xi\Xi\varXi
\pi\varpi\Pi\varPi
\rho\varrho
\sigma\Sigma\varsigma\varSigma
\tau\upsilon\Upsilon\varUpsilon
\phi\Phi\varphi\varPhi
\chi
\psi\Psi\varPsi
\omega\Omega\varOmega
\varOmega\varPhi\varPi$
\begin{lstlisting}
$\alpha\beta\gamma\Gamma\varGamma\delta\Delta\varDelta
\epsilon\varepsilon\lambda\Lambda\varLambda\zeta\eta\iota
\theta\Theta\vartheta\varTheta\kappa\varkappa\mu\nu
\xi\Xi\varXi\pi\varpi\Pi\varPi\rho\varrho\sigma\Sigma
\varsigma\varSigma\tau\upsilon\Upsilon\varUpsilon\phi\Phi\varphi\varPhi
\chi\psi\Psi\varPsi\omega\Omega\varOmega\varOmega\varPhi\varPi$
\end{lstlisting}

%小节
%\subsection{\zihao{-4} {\heiti subsection}}%小四号字、黑体、小节

%小小节
%\subsubsection{\zihao{-4} {\heiti subsubsection}}%小四号字、黑体、小小节

%参考文献
%\clearpage%另起一页
%\section{\zihao{4} {\heiti 参考文献}}%四号字、黑体的参考文献

%\begin{参考文献的表示方式}
%a)	书籍的表述方式为：
%[编号] 作者，书名，出版地：出版社，出版年，版次。
%b)	期刊杂志论文的表述方式为：
%[编号] 作者，论文名，杂志名，卷期号：起止页码，出版年。
%c)	网上资源的表述方式为：
%[编号] 作者，资源标题，网址，访问时间(年月日)。
%\end{参考文献的表示方式}

\end{document}
%\end{正文结束}
```

[查看全部 13 个回答](https://www.zhihu.com/question/29816700)