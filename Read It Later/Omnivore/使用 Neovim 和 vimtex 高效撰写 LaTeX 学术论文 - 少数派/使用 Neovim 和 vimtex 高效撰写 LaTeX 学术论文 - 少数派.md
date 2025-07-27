---
id: 6f47fe74-9ada-4ab4-beff-657f0197b36c

url: https://sspai.com/post/64080
status:
---


tags:: 

# 使用 Neovim 和 vimtex 高效撰写 LaTeX 学术论文 - 少数派
#Omnivore

[Read on Omnivore](https://omnivore.app/me/neovim-vimtex-la-te-x-18f66869228)
[Read Original](https://sspai.com/post/64080)

使用 Neovim 和 vimtex 高效撰写 LaTeX 学术论文

### Matrix 首页推荐

[Matrix](https://sspai.com/matrix) 是少数派的写作社区，我们主张分享真实的产品体验，有实用价值的经验与思考。我们会不定期挑选 Matrix 最优质的文章，展示来自用户的最真实的体验和观点。

文章代表作者个人观点，少数派仅对标题和排版略作修改。

---

LaTeX，作为学术界 de facto 的排版利器，其编辑器可谓是百花齐放。VS Code、TeXstudio、Texmaker，甚至在线的 Overleaf，虽然都可以拿来撰写 LaTeX 文档，但是它们的界面都相对臃肿，编译和预览速度上也不是「业内最快」。经历了近一个月的英文学术论文撰写，我发现直接使用被誉为「编辑器之神」的 Vim（实际上我使用的是 Neovim）来撰写 LaTeX，就我而言最为合适。使用 Neovim 编写 LaTeX 文献，不仅编译飞快、预览方便，还有着几乎无限的可定制性，唯一的缺点，**可能就是 Vim 自己相对陡峭的学习曲线。**

![](https://proxy-prod.omnivore-image-cache.app/0x0,s02Jr73YjIKo0Ksex8JaLw5-_uFd3bBYwOV-KeCxAXnk/https://cdn.sspai.com/2020/12/16/cb4b968f324a3dad791682528aa3fe7a.png?imageView2/2/format/webp)

在 Ubuntu 中使用 Neovim 撰写 LaTeX 论文，并使用 Zathura 预览生成的 PDF

在这篇文章里，我将不重点叙述 Vim 本身的使用方法，而是主要介绍使用 Vim 配合 LaTeX 发行版 TeX Live 和专为 Vim 设计的 LaTeX 插件 vimtex 来撰写 LaTeX 文献的配置技巧和方法。这一套技巧需要对 Vim 及其操作有着一定的了解，因此建议已经在使用 Vim 编辑文档或项目的同学，或者了解 Vim 的基础用法、希望使用 Vim 撰写 LaTeX 的同学参考本文。

## 基础知识

在正文开始之前，我先来简要的介绍一下 Vim 以及 LaTeX 的基础知识。

Vim 是一个在命令行环境下最能发光发热的纯文本编辑器，因此不论是 Linux、macOS 还是 Windows，只要我们安装了 Vim，那么我们只需要打开终端、使用命令 `vim`，即可进入 Vim 编辑器。**Neovim 是一个 Vim 的社区分支版本，比原版 Vim 有一些新增功能和喜人特性，我个人更喜欢使用 Neovim。**

Vim 是一个命令行环境下的编辑器，因此 Vim 自己并没有我们熟悉的 GUI 图形界面。如果在 Linux 和 macOS 下，那么使用各自系统的终端即可调用 Vim。如果在 Windows 上，我们则需要使用更为现代的终端，比如 [Windows Terminal](https://sspai.com/post/59380)，或者使用专为 Neovim 开发的 GUI 前端程序（也就是我们所称呼的 Neovim 前端），比如 [neovim-qt](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fequalsraf%2Fneovim-qt)、[FVim](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fyatli%2Ffvim) 等，才能提升使用 Vim 编辑的体验。在参考本文前，我们应该至少拥有一个完整的 Neovim 环境，包括 Neovim 本身以及 Neovim 前端。作为参考，我使用的是 Ubuntu 20.04.1 LTS、[Neovim v0.5.0-dev](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fneovim%2Fneovim) 以及 [kitty 终端](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fkovidgoyal%2Fkitty)。

### LaTeX 以及 TeX Live 发行版

LaTeX 是一个专业的排版引擎，其中包含有众多的宏包（撰写 LaTeX 文档时使用的依赖库）与编译器（比如输出 PDF 的 `pdflatex`、能够处理 UTF-8 与东亚字符的 `xelatex`、支持增量编译的 `latexmk` 等）。在参考本文前，我们需要在本机上[安装 TeX Live 发行版](https://sspai.com/link?target=https%3A%2F%2Fwww.tug.org%2Ftexlive%2Facquire-netinstall.html)才能完整拥有 LaTeX 环境，并用来编译、撰写 LaTeX 文档。我们将主要使用 `latexmk` 来编译 LaTeX 文档，`latexmk` 能够按需调用其他编译引擎，来根据文档内容（比如文档是否包含中文、文档中是否需要编译参考文档等）动态调整编译指令和编译内容。

### 撰写、预览 LaTeX 文档时，编辑器背后究竟在干什么？

很多集成度很高的编辑器（比如 TeXstudio）将编译 LaTeX 文档的整个过程隐藏在复杂的界面背后，实际上不易于我们理解 LaTeX 的完整编译闭环。因此，当我们在使用 Neovim 或者其他编辑器来撰写 LaTeX 文档时，我们实际上是做这样的一件事情：

* 我们使用纯文本编辑器（Neovim）编辑 `.tex` 文件的文本内容，也就是 LaTeX 文档本身；
* 在后台运行的 `latexmk` 发现我们的 `.tex` 文件内容发生了变化，于是开始编译新增内容：  
   * `latexmk` 会根据我们的 `.tex` 文件具体更改内容动态的调整编译命令和编译次数；  
   * 比如新增了参考文献的引用，则需要使用 `biber` 编译，或是增加了新的图表以及相应的引用，则需要两次至四次的调用 `pdflatex` 编译文档……
* 编译后会生成相应的 `.pdf` 文件来给我们预览，我们使用合适的 PDF 阅读器打开即可；
* 最后，同步编辑器和 PDF 阅读器的显示位置的任务，通常会使用 SyncTeX 来完成。

![](https://proxy-prod.omnivore-image-cache.app/0x0,syWTyLDAFCdezINyhNLbVGRLZFLYiZSyJQMxNs4fB5kI/https://cdn.sspai.com/2020/12/16/cd340a80a5b4a67652cc3716bacf745d.png?imageView2/2/format/webp)

编辑、编译 LaTeX 项目，并预览 PDF 时，背后发生的事情

整个编译过程就如图示所示，我们不论是使用 Neovim，还是使用其他集成度高的编辑器，背后实际上执行的都是这样的一套完整的流程。熟悉了整个 LaTeX 编译过程，我们接下来正式开始配置 Neovim 的 LaTeX 撰写环境。

## 使用 vim-plug 为 Neovim 安装 vimtex

Neovim 和 Vim 一样，都是极为可拓展的纯文本编辑器，有着社区无数的插件支持，我们将使用专业、极简的插件管理器 —— [vim-plug](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fjunegunn%2Fvim-plug) 来管理安装 Neovim 的插件。专为 LaTeX 编写设计的 [vimtex](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Flervag%2Fvimtex) 插件是 Neovim 撰写 LaTeX 的绝佳搭档，我们将使用 vimtex 来辅助我们在 Neovim 中撰写 LaTeX 项目。默认安装情况下，在 Linux 与 macOS 中的 Neovim 配置文件位于 `~/.config/nvim/init.vim`，在 Windows 中位于 `%LOCALAPPDATA%\\nvim\\init.vim`，我们后续的配置操作都将会直接更改这一配置文件。

首先我们安装插件管理器 vim-plug，对于 Neovim，在 Linux 或 macOS 中执行：

```roboconf
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
<https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim>'
```

或在 Windows 中执行：

```nginx
iwr -useb <https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim> |`
ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force
```

之后，我们需要在配置文件 `init.vim` 中添加 vim-plug 的插件定义部分：

```autoit
call plug#begin()
Plug 'xxx' # 这里即是安装某个插件的定义位置
Plug '...' # 可以继续定义其他需要安装的插件
# ……
call plug#end()
```

接下来，我们在定义安装插件的位置添加安装 vimtex 的定义字段。在 `init.vim` 中 vim-plug 插件定义部分添加：

```ada
Plug 'lervag/vimtex
```

之后，退出并重新进入 Neovim，执行命令 `:PlugInstall`，即可安装 vimtex 插件。

![](https://proxy-prod.omnivore-image-cache.app/0x0,s26WANJ-tWoY_q7ekGpUIIMNqvQ-K9pnxPo2iAS7QCkg/https://cdn.sspai.com/2020/12/16/9b09267ee6eba16c689f2cdc71909b4d.png?imageView2/2/format/webp)

成功安装 vimtex 插件

### 基础配置

在开始使用 vimtex 前，我们还需要配置一些设置项目。下面的全部配置内容都是需要写入配置文件 `init.vim` 的。首先，我们需要设置撰写的 TeX 文档是 LaTeX 语法风格的文档：

```vim
let g:tex_flavor = 'latex'
```

接下来，我们将编译报错自动弹出错误窗口（quickfix window）设置为 0（即不自动弹出）。我们可以使用命令 `:copen` 来手动打开错误窗口：

```nix
let g:vimtex_quickfix_mode = 0
```

### 预览 PDF 并使用 SyncTeX 同步位置

为了能够让 vimtex 自动在编译完成后启动 PDF 阅读器，我们需要指定所使用的 PDF 阅读器，不同操作系统使用的 PDF 阅读器也不尽相同，因此这里我会提供 Linux、Windows 以及 macOS 三种不同的 PDF 阅读器推荐配置，同学们按照自己的需要选择一种配置即可。

> Windows 与 macOS 的配置项目参考自：[A Complete Guide on Writing LaTeX with Vimtex in Neovim](https://sspai.com/link?target=https%3A%2F%2Fjdhao.github.io%2F2019%2F03%2F26%2Fnvim%5Flatex%5Fwrite%5Fpreview%2F)。

在 Linux 下我个人偏好使用 [Zathura 阅读器](https://sspai.com/link?target=https%3A%2F%2Fpwmt.org%2Fprojects%2Fzathura%2F)，我们这样定义即可：

```vim
let g:vimtex_view_general_viewer = 'zathura'
let g:vimtex_view_method = 'zathura'

# 这一项目默认即为 nvr，但是如果由于种种原因无法实现 SyncTeX 同步位置，可以考虑手动指定这一项目
let g:vimtex_compiler_progname = 'nvr'
```

此外我们还需要：

* 在系统 Python 环境下安装 [neovim-remote](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fmhinz%2Fneovim-remote)（也就是上面的 `nvr`）：

```cmake
pip3 install neovim-remote
```

* 单独安装 Zathura 并在其配置文件 `~/.config/zathura/zathurarc` 中加入下面内容：

```livecodeserver
# ~/.config/zathura/zathurarc
set synctex true
set synctex-editor-command "nvr --remote-silent %f -c %l"
```

在 Windows 上我们可以安装使用 [SumatraPDF](https://sspai.com/link?target=https%3A%2F%2Fwww.sumatrapdfreader.org%2Ffree-pdf-reader.html)，并在 `init.vim` 为 vimtex 配置如下内容：

```vim
let g:vimtex_view_general_viewer = 'SumatraPDF'
let g:vimtex_view_general_options
\ = '-reuse-instance -forward-search @tex @line @pdf'
let g:vimtex_view_general_options_latexmk = '-reuse-instance'
```

在 macOS 上我们可以安装使用 [Skim](https://sspai.com/link?target=https%3A%2F%2Fsourceforge.net%2Fprojects%2Fskim-app%2F)，并在 `init.vim` 为 vimtex 配置如下内容：

```vim
let g:vimtex_view_general_viewer
\ = '/Applications/Skim.app/Contents/SharedSupport/displayline'
let g:vimtex_view_general_options = '-r @line @pdf @tex'

" This adds a callback hook that updates Skim after compilation
let g:vimtex_compiler_callback_hooks = ['UpdateSkim']

function! UpdateSkim(status)
if !a:status | return | endif

let l:out = b:vimtex.out()
let l:tex = expand('%:p')
let l:cmd = [g:vimtex_view_general_viewer, '-r']

if !empty(system('pgrep Skim'))
call extend(l:cmd, ['-g'])
endif

if has('nvim')
call jobstart(l:cmd + [line('.'), l:out, l:tex])
elseif has('job')
call job_start(l:cmd + [line('.'), l:out, l:tex])
else
call system(join(l:cmd + [line('.'), shellescape(l:out), shellescape(l:tex)], ' '))
endif
endfunction
```

这样配置后，我们就可以通过 vimtex 默认的 `\lv` 快捷键（在按住 `\` 的时候，连续点击 `l` 和 `v`）来正向同步当前 Neovim 光标位置到 PDF 预览位置，也可以通过「`Ctrl` \+ 点击 PDF 预览相应位置」来反向同步 Neovim 光标位置了。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sWr3XyfIAnWGitX6mxHSL-MZ56F2gsEqQvkT_DQnkebs/https://cdn.sspai.com/2020/12/16/d71890ab30da487fe6633d307223020c.gif)

同步和反向同步 LaTeX 源码和预览 PDF 位置

### 使用 vimtex 编译、预览 LaTeX 项目

调用 vimtex 的编译预览以及其他相关命令，往往都会通过 vimtex 默认快捷键来进行操作。前面在配置同步 PDF 的时候，我们已经使用了一个常用的 vimtex 快捷键 `\lv`，实际上包括编译与自动唤起 PDF 阅读器、同步光标、停止编译以及清理中间无用文件的快捷键都是类似的操作：按住 `\` 键，并连续点击后续快捷键。下面是 vimtex 常见的默认快捷键：

* `\ll`：使用默认编译器（latexmk）开始监听 `.tex` 文件的变化，编译 LaTeX 项目并打开 PDF 预览界面；
* `\lk` 或第二次 `\ll`：停止编译器监听文件变动，停止编译；
* `\lv`：正向从 Neovim 光标位置同步 PDF 显示区域；
* `\lc`：清理编译生成的中间文件；

![](https://proxy-prod.omnivore-image-cache.app/0x0,s2NC1cTN4QkjHbL1Xnz9Tx7AT_JKbDki2grlAHh_UTXw/https://cdn.sspai.com/2020/12/16/49abcf3636080019f3ae6cbad1ccf679.gif)

基础的 vimtex 编译、同步位置等操作

其中，需要注意的一点是，前面提到的 `\` 键实际上是我们 Neovim 中设定的 local leader 键，如果没有特殊设置的话那么默认就是 `\` 键，但是如果有同学修改了这一键，那么需要按照自己的定义调整快捷键。

此外， vimtex 还包含有：

* 快速跳转至下一个或上一个 section 章节：`[[`、`]]`、`][`、`[]`；
* 删除包含当前内容的环境标签：`dse` (Delete surrounding environment)；
* 更换包含当前内容的环境标签：`cse` (Change surrounding environment)；
* 更换有 `*` 和无 `*` 的环境标签（比如将 `equation*` 更换为 `equation`、将 `figure*` 更换为 `figure` 等）`tse` (Toggle starred environment)：
* ……

等等一系列快捷键，用来提升我们的 LaTeX 项目编辑效率。上面是我自己常用的快捷键和快捷指令，更多快捷键请参考：[Features - lervag/vimtex](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Flervag%2Fvimtex%23features)。

### vimtex 的文章目录 TOC

vimtex 还有自动生成的 TOC 文章目录窗口，非常方便。我个人喜欢将 TOC 放置于左侧窗口，并移除一些非必要的信息板块，同时设定 TOC 窗口默认的宽度。我的 TOC 窗口配置如下：

```livescript
let g:vimtex_toc_config = {
\ 'name' : 'TOC',
\ 'layers' : ['content', 'todo', 'include'],
\ 'split_width' : 25,
\ 'todo_sorted' : 0,
\ 'show_help' : 1,
\ 'show_numbers' : 1,
\}

```

这样，我们使用命令 `:VimtexTocToggle` 即可唤出 vimtex 自动生成的 TOC：

![](https://proxy-prod.omnivore-image-cache.app/0x0,sD2SlJJF76hxdtneCr30OGfxMWj3U5eFfo4c1aBqGBIY/https://cdn.sspai.com/2020/12/16/26ccefded84d43a233d695cc43308e0c.png?imageView2/2/format/webp)

自动生成的 LaTeX 目录 TOC

## 使用 coc.nvim 自动补全 LaTeX 代码

虽然 vimtex 很优秀，但是许多比如自动补全、LaTeX 代码错误提示以及自定义 LaTeX 代码段等功能，还需要依赖其他插件的配合。[coc.nvim](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fneoclide%2Fcoc.nvim) 全称为 Conquer of Completion，是我在 Neovim 中偏好的自动补全引擎。由于 coc.nvim 支持了 VS Code 的 LSP 协议（Language Server Protocol），因此 coc.nvim 实际上能够做到类似 VS Code 级别的自动补全功能，这也是我使用 coc.nvim 的主要原因。

我们可以使用 vim-plug 来安装 coc.nvim，在 `init.vim` 的 vim-plug 部分加入如下内容，重新加载 `init.vim` 并执行 `:PlugInstall` 即可安装 coc.nvim。

```sml
Plug 'neoclide/coc.nvim', {'branch': 'release'}
```

此外，为了更好的配置 coc.nvim，我们还需要再额外添加一些 coc.nvim 的配置。coc.nvim 的 GitHub 主页给出了一个可以直接拿来使用的配置样例：[Example vim configuration - coc.nvim](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fneoclide%2Fcoc.nvim%23example-vim-configuration)，我们可以直接粘贴这部分代码进入 `init.vim` 之中。

最后，我们需要安装专为 vimtex 设计的 coc.nvim 插件：[coc-vimtex](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fneoclide%2Fcoc-vimtex)，在 Neovim 中执行 `:CocInstall coc-vimtex` 即可。这样，我们在撰写 LaTeX 文档时，就可以拥有如 VS Code 一样强大的自动补全功能了。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sqScJGtrhimun6TnH-ZC8yUh9T_Oi6TDCMrlV1F8txkg/https://cdn.sspai.com/2020/12/16/5ce7f9dd12cb19b570daa924c6567982.png?imageView2/2/format/webp)

coc.nvim 自动补全

## 使用 UltiSnips 快速输入预设 LaTeX 代码块

[UltiSnips](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2FSirVer%2Fultisnips) 是 Neovim 的 snippet 插件，也就是我们所说的「自定义代码段」。借助 snippet，我们可以快速输入预设代码段，包括常见的 LaTeX 代码。

我们可以使用 vim-plug 来安装 UltiSnips，在 `init.vim` 的 vim-plug 部分加入如下内容，重新加载 `init.vim` 并执行 `:PlugInstall` 即可安装 UltiSnips 以及配套的 snippet 库 [vim-snippets](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fhonza%2Fvim-snippets)，前者提供输入 snippet 的必要框架，后者提供多种语言的 snippet 预设代码块。

```sml
Plug 'SirVer/ultisnips'
Plug 'honza/vim-snippets
```

默认情况下我们在 insert 模式下可以使用 `Tab` 来自动扩展 snippet，常见的 LaTeX 代码块比如：

* 插入图片 Figure 环境，就可以用 fig + `Tab` 来自动扩展；
* 插入表格 Table 以及 Tabular 环境，就可以用 table + `Tab` 来自动扩展；
* 插入公式 Equation 环境，就可以用 eq + `Tab` 来自动扩展；
* ……

![](https://proxy-prod.omnivore-image-cache.app/0x0,shJyoyzlAiq3gR2FkNeOiKoNLjPTFuRan9rLCdwZf1Ko/https://cdn.sspai.com/2020/12/16/f439ffa3a7ceb62b90e88e41616b2fc2.gif)

使用 UltiSnips 快速输入预设 LaTeX 代码块

## 小结

相信很多使用 LaTeX 的同学都可能读过一篇叫做[《How I'm able to take notes in mathematics lectures using LaTeX and Vim》](https://sspai.com/link?target=https%3A%2F%2Fcastel.dev%2Fpost%2Flecture-notes-1)的文章，在这篇文章中，作者详细的介绍了自己是如何通过熟练的 Vim 技巧，加上合适的 snippet 以及自动补全，来使用 LaTeX 和讲座进度几乎同步的记录总结，最终得到格式严格、排版整洁，却无需任何课后额外时间整理的完美笔记。

![](https://proxy-prod.omnivore-image-cache.app/0x0,s6nx0eT-wo_FIx-SYDqA9rPXNUydxnuNsGl7YXLxnTv0/https://cdn.sspai.com/2020/12/16/95df688ffdee5671df8fbb80521c37b0.png?imageView2/2/format/webp)

来自 How I'm able to take notes in mathematics lectures using LaTeX and Vim 一文中的笔记

我就是因为这样的一篇文章，才意识到使用 Vim 来撰写 LaTeX 是能够如此的提升我的文献撰写效率。虽然本文的配置远远没有那位作者的复杂，但是我相信我的配置方案能够帮助许多同学在初次配置自己撰写 LaTeX 项目的 Vim 或 Neovim 时少走很多弯路。感谢阅读。

\> 下载少数派 [客户端 ](https://sspai.com/page/client)、关注 [少数派公众号 ](https://sspai.com/s/J71e)，了解更妙的数字生活 🍃

\> 想申请成为少数派作者？[冲！](https://sspai.com/apply/writing)

© 本文著作权归作者所有，并授权少数派独家使用，未经少数派许可，不得转载使用。

