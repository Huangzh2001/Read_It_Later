---
id: f9bdea16-5eb8-41b4-924d-d6963afab84d
---


tags::  #Readed 

# 【Python】输入 LaTeX 代码并通过 Sympy 完成计算或化简 - MowChan - 博客园
#Omnivore

[Read on Omnivore](https://omnivore.app/me/python-la-te-x-sympy-mow-chan-19072faff93)
[Read Original](https://www.cnblogs.com/mowchan/p/calculate-latex-formula-by-sympy.html)

Sympy 是常用的一个符号计算的 Python 库，基本可以满足初等数学到高等数学、线性代数、离散数学以及本科物理所需的符号计算。然而 Sympy 在使用时还需要声明变量，并使用类 Wolfram 的语法格式表示数学表达式，在录入大量的数学公式时明显不便。而 LaTeX 代码无论在国外的排版还是国内外 Web 端的数学公式渲染实现上都是事实的标准，方便使用。

因此，本文介绍一个将 LaTeX 代码转换为 Sympy 对象的模块，并总结使用过程中的一些问题。

### 安装 latex2sympy2 而不是 latex2sympy

不要使用 latex2sympy，latex2sympy 已不再更新维护，功能匮乏。OrangeX4 二次开发的 latex2sympy2 不断更新，实现了更多功能，推荐使用。

**安装 latex2sympy2**（依赖包括 Sympy，建议安装 1.8.x 及其以上版本）

```cmake
pip install latex2sympy2

```

### latex2sympy2 基本功能

```angelscript
from latex2sympy2 import latex2sympy, latex2latex

```

`latex2sympy` 将 LaTeX 代码转换为 Sympy 实例后作计算化简，便于进一步处理；

`latex2latex` 将 LaTeX 代码转换为 Sympy 实例计算化简后以 `str` 格式输出，如求微分 d(x2+x)dx

```python
>>> latex2sympy(r"\frac{d}{dx}(x^{2}+x)")`
Derivative(x**2 + x, x)

>>> latex2latex(r"\frac{d}{dx}(x^{2}+x)")`
'2 x + 1'

```

（注意，输入的 LaTeX 字符串前应有反转义符 `r`）

除了常规的计算，latex2sympy2 还**支持识别特殊格式**，如 display 模式的分数 `\dfrac`，绝对值 `|`，拉伸括号的命令 `\left`、`\right` 等。

注意，小学数学中的**带分数**（mixed number）在 LaTeX 中是没有实现标准的，因此是无法直接正确计算的，如 213 的 LaTeX 代码是 `2 \frac{1}{3}`，会被识别为 `2 * 1 / 3` 即 23。所以应当在整数部分和分数部分之间加入加号，`2 + \frac{1}{3}`。

### 代数式中代入求值

latex2sympy2 中提供特殊语法，实现代入具体的数值对代数式化简求值，语法格式如下

`(代数式)|_{变量=值}`

若代入多个变量的值，应当写为

`(代数式)|_{变量1=值}|_{变量2=值}|_{变量3=值}`

如将 x\=−2 代入 x3−9(x−2)2+(y−2)3−9，

```python
>>> latex2latex(r'( x^3 - 9(x-2)^2 + (y-2)^3 - 9)|_{x = -2}')
'(y - 2)^{3} - 161'

```

将 x\=−2，y\=1 代入 x3−9(x−2)2+(y−2)3−9，

```python
>>> latex2latex(r'( x^3 - 9(x-2)^2 + (y-2)^3 - 9)|_{x = -2}|_{y = 1}')
'-162'

```

### 解方程组、不等式组的实现封装

latex2sympy 可以直接求解 LaTeX 方程，但是不能解方程组和不等式组。这里我提供一个解方程组、不等式组的实现函数。

```python
from re import findall, split, MULTILINE
from sympy import solve as solving, latex
from latex2sympy2 import latex2sympy, latex2latex


def solve(latex_text, formatter='sympy'):
    regex = r"\\begin{cases}([\s\S]*)\\end{cases}"
    matches = findall(regex, latex_text, MULTILINE)
    equations = []
    if matches:
        matches = split(r"\\\\(?:\[?.*?\])?", matches[0])
        for match in matches:
            ins = latex2sympy(match)
            if type(ins) == list:
                equations.extend(ins)
            else:
                equations.append(ins)
        solved = solving(equations)
    else:
        return False
    if formatter == 'latex':
        return latex(solved)
    else:
        return solved

```

函数默认输出 Sympy 对象，可以更改参数输出 LaTeX。

```awk
solve(r"latex code", formatter="latex")` 

```

下面提供一些计算的实例：

**一、解含分式的不等式组**

{5x+4⩾2(x−1)2x+53−3x−22\>1

```tex
>>> solve(r'\begin{cases} 5x+4 \geqslant 2(x-1) \\\\[1.5ex] \dfrac{2x+5}{3}-\dfrac{3x-2}{2}>1 \end{cases}', formatter='latex')
'-2 \leq x \wedge x < 2'

```

解得：−2⩽x∧x<2

**二、解二元一次方程组**

{3x\=2y8x+5y\=−31

```python
>>> solve(r'$\begin{cases} 3x=2y \\\\[1.5ex] 8x+5y=-31 \end{cases}$')
{x: -2, y: -3}

```

解得：{x:−2, y:−3}

**三、解三元一次方程组**

{x+y−z\=11x+z−y\=1y+z−x\=5

```python
>>> solve(r'\begin{cases} x+y-z=11 \\\\[1.5ex] x+z-y=1 \\\\[1.5ex] y+z-x=5 \end{cases}')
{x: 6, y: 8, z: 3}

```

解得：{x:6, y:8, z:3}

**四、方程组无解**

{−6x+3y\=92x−y\=1

```python
>>> solve(r'\begin{cases} -6x+3y=9 \\\\[1.25ex] 2x-y=1 \end{cases}')
[]

```

方程组无解

### 参考文章

* [latex2sympy2 · PyPI](https://pypi.org/project/latex2sympy2/)
* [Python干货之科学计算工具SymPy大全 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/337412103)

posted @ [MowChan](https://www.cnblogs.com/mowchan)阅读(3125) 评论() [编辑](https://i.cnblogs.com/EditPosts.aspx?postid=17065458)收藏 举报

