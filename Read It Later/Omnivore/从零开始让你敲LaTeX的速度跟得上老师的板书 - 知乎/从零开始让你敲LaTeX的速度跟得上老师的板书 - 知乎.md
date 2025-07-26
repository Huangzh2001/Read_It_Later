---
id: e81e1902-abd5-4c2a-95f3-dd9a4135d542
---


tags::  #Readed 

# 从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/la-te-x-18f481cbf31)
[Read Original](https://zhuanlan.zhihu.com/p/501582548)

本文将从零开始教你如何安装Emacs+AuCTeX+CDLaTeX。一位熟练使用这些工具的数学系学生可以在上课用LaTeX记笔记并跟上老师讲课的速度。本文所描述的路径不一定是最优的，但一定是笔者亲自实践过的。

另：本文基本上是网上各种教程与官网教程的缝合怪，写完发现忘了留referrence了在此表示抱歉。后来重走了一遍，留下一份记录可作参考：[方汝见之：简单记录重启 Linux 之旅](https://zhuanlan.zhihu.com/p/695753073)。

建议在网络较好的地方执行本教程，或者找点什么能够打发漫长的下载与等待过程的事……

## 0.Linux虚拟机的配置

若您已经配置好了一个Linux系统，则您可以跳过这一节。

本文在Linux系统Ubantu上配置GNU Emacs。为此笔者使用了虚拟机而非双系统。

VMware Workstation player是免费的虚拟机软件，其下载链接如下：

[https://customerconnect.vmware.com/en/downloads/details?downloadGroup=WKST-PLAYER-1623-NEW&productId=1039&rPId=85399](https://link.zhihu.com/?target=https%3A//customerconnect.vmware.com/en/downloads/details%3FdownloadGroup%3DWKST-PLAYER-1623-NEW%26productId%3D1039%26rPId%3D85399)

按提示安装即可。

（仅有支持母机为Windows与Linux系统的版本，Mac系统可以考虑一下Virtual Box，下载链接：[VirtualBox Mac官方版-VirtualBox for Mac(虚拟机软件)- Mac下载](https://link.zhihu.com/?target=https%3A//www.macz.com/mac/3565.html%3Fid%3DNzY4OTU4Jl8mMjcuMTg3LjIyNy4xNzk%253D))

对于Linux系统，笔者选择了Ubuntu 20.04.4 LTS，其光盘镜像的官方下载链接为：[下载Ubuntu桌面系统 | Ubuntu](https://link.zhihu.com/?target=https%3A//cn.ubuntu.com/download/desktop)（文件较大(3.1G)，建议在网络较好处下载）。

个性化部分请凭自己喜好设置，但仍建议设置较简单的密码并背下来，该密码将经常被输入。由于LaTeX文件很大，建议为虚拟机预留40G的磁盘空间。

然后用该光盘镜像文件创建虚拟机：

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/1377a90b6f5446d8b125590fb1599f06_MD5.jpg]]

由于LaTeX体积较大，建议多预留一些存储空间，比如40G

然后是漫长的等待系统安装完成（笔者这边网速欠佳等待了40分钟之久）。按Ctrl+Alt可以返回母机（以防读者因为鼠标被黑屏吞没不知所措）。

在系统安装完成后，我们来进行一些基础配置。

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/45c51269578c1d5de0209353da0207dd_MD5.jpg]]

点击左下角的九宫格以打开应用列表（再次点击可以关闭）。点击Language support，系统会提示你语言包安装不完整安装即可。点击Install/Remove Languages，选择Chinese (simplified)，点击Apply，然后继续漫长的等待。

当然这个下载过程是可以后台进行的。现在让我们做一点别的工作。

首先再次点击左下角的九宫格，找到Terminal（终端），右键点击，选择Add to Favorites。我们会经常地用到终端，把它放在快捷栏是方便的。

让我们打开终端学习最基础的Linux指令。

* 首先是`sudo` (super user do 的缩写)，相当于Windows系统的“用管理员身份打开”。打开终端后第一次输入带sudo的指令后终端会提示你输入密码，而这个输入过程是没有回显的。
* 然后是`ls`，显示当前目录下的所有文件
* 最后是`cd`，其后接文件路径。这个路径可以是相对于当前目录的相对路径，也可以是绝对路径。路径以/分隔层级，以..表示返回上一级。cd后什么都不接将返回根目录。你可以试着输入 `cd Desktop`来访问桌面，再输入`ls`以查看桌面上的文件列表。输入时试着按`[Tab]`用自动补全加快输入速度。
* `mkdir`是创建文件夹的指令，注意前面不要接`sudo`。删除文件夹是`rm`（即我们常说的remake）。永远不要在根目录输入`rm -rf`：这表示删库跑路。
* 再遇到什么指令上网查即可，本文只需要你复制粘贴。多看也就知道是什么意思了。Ubantu有着强大的图形界面，也不必强求事事用命令行。

等语言包安装好了，我们回来把汉语（中国）拖到上面，点击Apply System-Wide，关闭后再重启虚拟机（左上角暂停图标的下拉栏有重启选项）便可以应用中文界面了。**重启后会提示是否汉化目录，请选择否**（否则再把语言调成英文再逆汉化回来吧……）。这是因为LaTeX不能编译保存路径中有中文的文件。

下面让我们来配置中文输入法。点击左下角，找到设置-区域与语言，点击加号-汉语-中文（智能拼音）并把它拖到上面来，再重启即可。

## 1.GNU Emacs的配置

打开终端，输入GNU Emacs的官网安装教程（[GNU Emacs download - GNU Project](https://link.zhihu.com/?target=https%3A//www.gnu.org/software/emacs/download.html)）中的指令：

```routeros
sudo apt-get install emacs
```

（若你的Linux系统版本不同，可能需要官网提供的其它指令）

现在我们已经成功安装了Emacs。点开左下角，可见Emacs的GUI（图形用户界面）和终端。

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/f04c46363f98ab5137c37a3a104b8c31_MD5.jpg]]

现在你可以点击进入Emacs的GUI并阅读Emacs Tutorial。

要用Emacs打开文件，只需在终端输入（如无必要不要加`sudo`）

若文件名不存在，这将建立一个新的文件。这样也会进入Emacs的GUI。

> 若你满足于轻量化的所见即所得的做笔记需求，现在你可以去([https://orgmode.org/](https://link.zhihu.com/?target=https%3A//orgmode.org/) ) 学习Org mode的使用方法并跳到安装CDLaTeX的部分。但是要轻量化为什么不选择Markdown呢……  
> 为使用Markdown，若你懒得配置VScode，你可以试试marktext）

为了快速上手Emacs，笔者这里罗列一些打LaTeX所需的指令：

* Emacs有两个功能键，C表示CONTROL键，对应键盘上的Ctrl；M表示Meta键。一般约定`C-<chr>` 表示当输入字符 `<chr>` 时按住 Ctrl 键，`M-<chr>` 表示当输入字符 `<chr>` 时按住 Meta 键。注意你可以一直按住CONTROL或META键来连续打两个指令：`C-<chr1> C-<chr2>`。你所打出的命令会在Emacs窗口最底下的缓冲区显示。
* `C-g`终止命令，`C-x C-c`退出Emacs，`C-_ `，`C-/`，` C-x u`都是撤销指令。
* `C-x C-s`储存文件
* 移动光标当然可以使用上下左右键，但Emacs还提供`C-p, C-n C-b C-f`分别实现光标的上、下、左、右移动。
* 翻页当然可以使用PageUp与PageDown，或者直接把光标移动到页底使其自动翻页等，但Emacs提供的`C-v`（向下翻页）和`M-v`（向上翻页）同样是便利的。
* `C-a C-e`分别将光标移动到一行的头部/尾部
* `C-x (数字)`表示留下（数字）个窗格（一般是1，用于关掉额外的窗格）。可以点击窗格下面的Buffer name（即加粗的文件名）来切换窗格的内容。
* 插入与删除单个文字的方法与Windows系统无异，只是需要注意插入或删除的位置在光标所覆盖字符的前面
* 欲选定一段文字，首先在其开头（或结尾）输入`C-<SPC>`（即`C-`空格键，或者`C-@`）并将光标移动到另一端，按`C-w`剪切/`M-w`复制。再按`C-y`进行粘贴。

打LaTeX常用到的指令大概就这些，有兴趣进一步了解的读者可以花点时间阅读Tutorial或找一本相关书籍等等。

最后为了美观，你可以在工具栏的Options里修改字体、主题等。

## 2\. TeX Live的配置

> 此处教程较老旧，建议换国内源下载安装，流程是一样的。

据说apt-get安装的版本较老，故我们按照官网教程的步骤安装TeX Live:

首先进入[Installing TeX Live over the Internet - TeX Users Group](https://link.zhihu.com/?target=https%3A//tug.org/texlive/acquire-netinstall.html)，点击 \[install-tl-unx.tar.gz\]。**下载选项请选择Save File**。

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/ecec8e730d8f2fdfbc01c392ef75ae02_MD5.jpg]]

若选择Open with, 打开再关闭后文件就会被删除

文件会在“下载”文件夹中。将其原地解压缩。

（此处官网建议安装 LWP perl package以加快安装速度，这里就不费这个事了）

打开终端，cd到解压缩所得文件夹再深入一层（直到`ls`后能看见install-tl这个文件），然后输入

之后终端会提示你输入指令，输入`i`即可。当然你也可以用`sudo perl install-tl -gui`用图形化界面安装。

下面进入更加漫长的等待……

（ Windows 不需要）安装成功后需要配置路径（就如终端提示你的那样）。输入

```awk
sudo emacs /etc/environment
```

这便打开了路径信息文件。笔者的终端这里提示到：

```routeros
Add /usr/local/texlive/2022/texmf-dist/doc/man to MANPATH.
Add /usr/local/texlive/2022/texmf-dist/doc/info to INFOPATH.
Most importantly, add /usr/local/texlive/2022/bin/x86_64-linux
```

于是我们向配置文件中写入

```ini
MANPATH="/usr/local/texlive/2022/texmf-dist/doc/man"
INFOPATH="/usr/local/texlive/2022/texmf-dist/doc/info"
PATH="/usr/local/texlive/2022/bin/x86_64-linux"
```

`C-x C-s`保存即可。

修订：笔者此后又尝试了若干次安装texlive，但总以把电脑搞崩收尾。建议直接配置MiKTeX。

### 3\. MiKTeX的配置

请按你的操作系统选择安装 MikTeX 的方式。

如果你只用到最基础的宏包，或者学会用tlmgr管理宏包，那么这一步是可以跳过的，毕竟笔者就这么用了半年。

在安装AuCTeX之前，让我们先安装用于管理宏包的MiKTeX。

在终端依次输入

```vim
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D6BC243565B2087BC3F897C9277A7293F59E4889
echo "deb http://miktex.org/download/ubuntu focal universe" | sudo tee /etc/apt/sources.list.d/miktex.list
sudo apt-get update
sudo apt-get install miktex
```

完成上述操作后，你可以点击左下角的九宫格找到MiKTeX Console并按提示完成配置。

## 4\. AuCTeX的配置

注意这里不可以使用`apt-get install auctex`安装auctex，除非你是用同样的方法安装的TeX Live。

官网推荐的安装AuCTeX方式为：打开Emacs终端，输入`M-x list-packages`，回车，找到AuCTeX并在那一行输入`i`，再按`x`安装。当然直接输入`M-x package-install` `auctex`来安装它。

现在根目录还没有`.emacs`文件，我们需要手动建立一个（如果读者那里有直接访问即可：注意这是隐藏文件须在文件管理按`Ctrl+h`显示隐藏文件）。

打开终端，回到根目录（或者直接打开新的终端），输入`emacs .emcs`，并在所打开的文件中键入以下内容：（这是用Lisp语言写成的）

```lisp
(load "auctex.el" nil t t)
;; 下面这行有时会导致bug，若出现问题请注掉
(load "preview-latex.el" nil t t)
(setq TeX-auto-save t)
(setq TeX-parse-self t)
(setq-default TeX-master nil)
(setq TeX-output-view-style (quote (("^pdf$" "." "evince %o %(outpage)"))))
(add-hook 'LaTeX-mode-hook
(lambda()
(add-to-list 'TeX-command-list '("XeLaTeX" "%`xelatex%(mode)%' %t" TeX-run-TeX nil t))
(setq TeX-command-default "XeLaTeX")))
```

现在你已经可以在emacs里写LaTeX了！

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/36a23a565dc6e3a1e89bdf6949edd0a5_MD5.jpg]]

在Windows上怎么写LaTeX在这里就怎么写

> 在 Windows 上，为防止中文乱码，你可能需要在文件开头加入如下代码：

编译的快捷键是`C-c C-c`，但更常用的是编译并展示：`C-c C-a`。除此之外还有一些常用的快捷键，你可以在工具栏的LaTeX,Command等栏目中查看它们。这里列举一些常用的快捷键：

* `C-c C-e`插入环境（\\begin{}……\\end{}）
* `C-c C-s`插入层次（section, paragraph等）
* `C-c C-j`或`M-[RET]`插入条目
* `C-c C-f C-b`粗体（\\textbf）：字体相关指令都以`C-c C-f` 开头。
* C-c \` 下一个错误

但是很多自动补全功能还没有实现。为此点击工具栏的LaTeX-Customize AUCTeX-Browse Options，搜索并调整以下变量：（调整后点击 Apply and Save）

* `TeX-electric-math`，这个变量实现的是自动插入两个$，以及可以在输入$时自动输入\\(\\)——有助于和evil-tex配合。
* `LaTeX-electric-left-right-brace`，这个变量实现自动补全括号
* `TeX-electric-sub-and-superscript`，这个变量实现在输入上、下标时自动加入大括号

对于更多功能请查阅文档[AUCTeX 13.1: Table of Contents](https://link.zhihu.com/?target=https%3A//www.gnu.org/software/auctex/manual/auctex/auctex%5Ftoc.html%23SEC%5FContents) 

## 5\. CDLaTeX的配置

最后是配置CDLaTeX。为此首先配置melpa源。在.emacs文件中加入如下内容：

```scheme
(setq package-archives '(("gnu"    . "http://mirrors.tuna.tsinghua.edu.cn/elpa/gnu/")
                         ("nongnu" . "http://mirrors.tuna.tsinghua.edu.cn/elpa/nongnu/")
                         ("melpa"  . "http://mirrors.tuna.tsinghua.edu.cn/elpa/melpa/")))
(package-initialize) 
```

然后重启Emacs，再 M-x package-install \[RET\] cdlatex 即可。为在写LaTeX时使用cdlatex，我们在.emacs文件中加入

```lisp
(add-hook 'LaTeX-mode-hook 'turn-on-cdlatex)
```

CDLaTeX的使用很简单。以下内容取自其README文档([cdlatex/README at master · cdominik/cdlatex · GitHub](https://link.zhihu.com/?target=https%3A//github.com/cdominik/cdlatex/blob/master/README))。

`C-c {`插入环境（这在 org mode 是很方便的）。对于大多数常用环境，你可以使用缩写+`[TAB]`来生成。例如equ\[TAB\]将生成  
 \\begin{equation} \\end{equation}  
 按`C-c ?`以查看所有支持的缩写，其完整的列表如下：（其中包含一些常用数学指令，如`\frac` )

```sql
pref Make page reference TEXT/MATH
ref Make reference TEXT/MATH
lbl Insert automatic label at point TEXT/MATH
ct Insert \cite TEXT/  
cte Make a citation interactively TEXT/  
cite{ Make a citation interactively TEXT/  
beg Complete an environment name and insert template TEXT/MATH
env Complete an environment name and insert template TEXT/MATH
it New item in current environment TEXT/MATH
ite Insert an ITEMIZE environment template TEXT/  
enu Insert an ENUMERATE environment template TEXT/  
equ Insert an EQUATION environment template TEXT/  
eqn Insert an EQUATION environment template TEXT/  
ali Insert an ALIGN environment template TEXT/  
ali* Insert an ALIGN* environment template TEXT/  
alit Insert an ALIGNAT environment template TEXT/  
alit* Insert an ALIGNAT* environment template TEXT/  
xal Insert a XALIGNAT environment template TEXT/  
xal* Insert a XALIGNAT* environment template TEXT/  
xxa Insert a XXALIGNAT environment template TEXT/  
xxa* Insert a XXALIGNAT environment template TEXT/  
mul Insert a MULTINE environment template TEXT/  
mul* Insert a MULTINE* environment template TEXT/  
gat Insert a GATHER environment template TEXT/  
gat* Insert a GATHER* environment template TEXT/  
spl Insert SPLIT environment template /MATH
fla Insert a FLALIGN environment template TEXT/  
fla* Insert a FLALIGN* environment template TEXT/  
fg Insert a FIGURE environment template TEXT/  
sn Insert a \section{} statement TEXT/  
ss Insert a \subsection{} statement TEXT/  
sss Insert a \subsubsection{} statement TEXT/  
pf Insert a \paragraph{} statement TEXT/  
sp Insert a \subparagraph{} statement TEXT/  
ssp Insert a \subsubparagraph{} statement TEXT/  
cl Insert \centerline TEXT/  
inc Insert \includegraphics with file name TEXT/  
lr( Insert a \left( \right) pair /MATH
lr[ Insert a \left[ \right] pair /MATH
lr{ Insert a \left{ \right} pair /MATH
lr< Insert a \left\langle \right\rangle pair /MATH
lr| Insert a \left| \right| pair /MATH
caseeq Insert a = { construct /MATH
fr Insert \frac{}{} /MATH
sq Insert \sqrt{} /MATH
intl Insert \int\limits_{}^{} /MATH
suml Insert \sum\limits_{}^{} /MATH
nonum Insert \nonumber\\ /MATH
fn Make a footnote TEXT/  
qq Insert \quad TEXT/MATH
qqq Insert \qquad TEXT/MATH
```

输入1-3个\`\`\` \`\`加上单个字符可以输入常用数学符号。例如：输入

的效果是\\epsilon。详尽的符号表可以查看按\`\` \`后静置一秒后显示的提示，这里笔者将其截图如下：

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/a2c2a8773a7f28176be189027d83f395_MD5.jpg]]

一个\`

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/7b2875d7db6866e5c5a7ab5af4deb012_MD5.jpg]]

两个\`

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/92c4ea10509391269c70ccc9c1adcac4_MD5.jpg]]

三个\`

在一段文字或公式后打`'`加上一个字母将依是否是数学环境改变前面文字（默认为一个词，以大括号为界）的字体。同样地，打出`'`后静置一秒将显示所有可用相关指令：

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/3429a8b1a4223b95b3dced510151e059_MD5.jpg]]

数学环境中

![[Omnivore/从零开始让你敲LaTeX的速度跟得上老师的板书 - 知乎/attachments/b939110b83b218752e57c63c5e7faa0c_MD5.jpg]]

非数学环境中

（第一行第三个符号是`~`）

当然，要正常打出`'`，只需按两次`'`。

CDLaTeX实现了上面我们所配置的AuCTeX的自动补全功能，但额外添加了按两次`^`将输入`^{\rm }`的功能，当然`_`同理（需在工具栏找到并手动开启）。

当你不知道要干什么，按`[TAB]`就完了。`[TAB]`被重载了以下功能：扩展缩写、取消仅一个字符的上下标的大括号、跳到下一个输入点（用于复杂的环境模板）……

## 6\. 其它

这里分享几个能够提高输入效率的网站，都是其它知乎er推荐过的：

1. [Detexify LaTeX handwritten symbol recognition](https://link.zhihu.com/?target=http%3A//detexify.kirelabs.org/classify.html) 识别手写LaTeX符号（加载较慢，建议如果预见到需要它请在打开LaTeX前打开它，或者用你解决stack exchange速度过慢的方式解决这一问题）
2. [Create LaTeX tables online – TablesGenerator.com](https://link.zhihu.com/?target=https%3A//tablesgenerator.com/) 在线制作表格并转为LaTeX语句
3. [https://tikzcd.yichuanshen.de/](https://link.zhihu.com/?target=https%3A//tikzcd.yichuanshen.de/) 在线画交换图并转为LaTeX语句（注意交换图需要ticz-cd 宏包，交换图代码需在数学环境内）

作为更轻量化的工具，Emacs 的 Org mode 是非常好的选择——尤其是最近的更新大幅提高了预览 LaTeX 的效率，因其学习成本较高有兴趣者可自行了解。

Emacs 和 Vim 作为世界上最好的两大编辑器，前者追求尽可能大包容万物，后者追求尽可能小嵌入万物。当我们把尽可能小的 Vim 嵌入尽可能大的 Emacs，在 Emacs 中使用 Vim 的键位编辑文本，我们便得到了——Emacs 的 evil mode！启用 evil mode 写 LaTeX 需要额外安装 evil 以及 evil-tex, evil-surrond 等，然后在 .emacs 文件中加入

```lisp
(evil-mode 1)
(add-hook 'LaTeX-mode-hook #'evil-tex-mode)
(global-evil-surround-mode 1)
```

还有一些能够提升效率的工具，在此列出：

* 用 M-x package-install \[RET\] yasnippet 即可安装yasnippet。为此，只需在.emacs文件中加入：
* 【限 linux】Zathura是更优的pdf阅读器（Windows 可以用 Sumatra pdf），可以配置向前向后搜索。其官网为([pwmt.org](https://link.zhihu.com/?target=https%3A//pwmt.org/projects/zathura/))。用 apt-get install 的方式也许无法得到最新版但绝对能用。再于.emacs文件中添加以下代码以启用zathura作为pdf阅读器：

```scheme
(setq TeX-view-program-selection '((output-pdf "Zathura"))) 
(setq TeX-view-program-list '(("Zathura" "zathura %o")))
```

* 笔者自己用于提升打字效率的软件是金山打字通，建议直接从打单词开始练习背下来按键的相对位置速度就上来了。另建议使用小鹤双拼和小鹤音形。
* preview-latex的使用见Emacs的菜单栏，只需注意不要预览含中文的标题（section,paragraph名）即可。
* prettify-symbols-mode 并不能提升速度，但可以让代码赏心悦目。只需在.emacs中加入：

```clojure
(global-prettify-symbols-mode 1)
```

* 可以用 Highlight-Parentheses 包来配置意义不明的彩虹括号（颜色可以手动再调），为此只需于 .emacs 中加入如下代码：

```lisp
(define-globalized-minor-mode global-highlight-parentheses-mode
  highlight-parentheses-mode
  (lambda ()
    (highlight-parentheses-mode t)))
(global-highlight-parentheses-mode t)
```

* RefTeX 已预安装在新版本的 Emacs 中。有了它，你可以方便地用 C-c ( 来写label，用 C-c ) 来引用。为启用它，只需在 .emacs 中加入

```scheme
(require 'reftex)
(add-hook 'LaTeX-mode-hook 'turn-on-reftex)
```

* 以及有问题为什么不问问万能的ChatGPT呢。

最后，上述教程只是配置了快速打LaTeX的工具，真正要提高输入效率，还是两个字：“多练”。

