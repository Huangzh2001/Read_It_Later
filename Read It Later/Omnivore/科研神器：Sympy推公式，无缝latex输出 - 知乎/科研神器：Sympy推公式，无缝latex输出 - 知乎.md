---
id: 824516de-90b8-456a-9ad7-a89c9e5882c5

url: https://zhuanlan.zhihu.com/p/491831883
status:
---


tags::  #Readed 

# 科研神器：Sympy推公式，无缝latex输出 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/sympy-latex-19072ede6ca)
[Read Original](https://zhuanlan.zhihu.com/p/491831883)

最近升级了一下自己的工作流，一是用上了latex，配合Mathpix Snipping一步到位，直接跳过latex公式语法的入门；二是sympy辅助推公式，省去了不少机械化简和mathtpye手打公式的时间。上面的过程都可以在VScode下完成，工作流无缝衔接。简单记录下过程，和大家分享。

Latex与word最大的区别是：Word所见即所得，Latex所写即所得。Latex可以所写即所得，是因为排版格式都通过代码唯一标示了。 

支持Latex的工具有很多，最简单的可以使用在线Latex工具，比如Overleaf。Overleaf上有很多模板可以直接使用，除常用的期刊论文模板外，还有大论、报告、PPT、甚至学术海报的模板，基本将常规需求一网打尽，如下面截图。 

![[Omnivore/科研神器：Sympy推公式，无缝latex输出 - 知乎/attachments/24b14f8ee288fa7bd9f44d27b6ed81cb_MD5.png]]

Overleaf 的文件都存在云端，可以通过浏览器在线访问，也可以将文档分享给合作者一同编辑，付费升级后能解锁更多的在线合作功能。

除了Overleaf，也可以本地配置Latex环境，Mac系统下一般会用MacTex，在终端下通过brew可以一键安装，如下面截图。当然，也可以装不带图形界面的版本mactex-no-gui。

![[Omnivore/科研神器：Sympy推公式，无缝latex输出 - 知乎/attachments/67a5aa5065db035667060b78e222d6e4_MD5.png]]

 配置好环境后，可以直接用Mactex自带的编译器编译，也可以用VScode。我个人更喜欢VScode，因为可以和自己写的代码无缝衔接。具体的配置方法，可以参考下面帖子：

 当然，直接使用Latex也有不太方便的地方——不太适合当草稿用。当一个想法还不太成熟的时候，我们往往不能有序地输出可供排版的内容，这时候Word的优势会体现出来，可以随时写下想法，从各种网站论文上截图，任意标注添加批注等。因此，Latex更时候体系想法成熟，开始输出的时候用。

本小节最后，推荐一个写的很赞的Latex教程，传送门如下：

## 二. Mathpix Snipping 编辑公式

使用Latex的最大的障碍之一就是要用Latex的语法打公式，对于新手来说十分不友好。为此，可以祭出Mathpix Snipping，它是支持手机、电脑、平板多平台的公式代码转化软件。安装后，可以直接截图「或者照片」识别公式，输出Latex代码。也可能在平板上手写公式，同样能自动识别。

下面就是我截图的一个论文里的公式，然后转换出的代码，亲测准确率高达99.9%，只有少数过于复杂且带标注的公式会识别错误。截图识别的另一个好处，是避免手打很多约定俗成的公式，直接从文献或者书里面截图识别极大地减少了手撸公式的工作量。

![[Omnivore/科研神器：Sympy推公式，无缝latex输出 - 知乎/attachments/fd2b206af06d0f1a89edf4c18fd14c63_MD5.png]]

## 三. Sympy推公式，无缝Latex输出

最后一个工具是Sympy，可以用来推公式和化简，这也是我最近才发现的一个宝藏工具，之前一直手推和化简，确实过于天真…… 下面是一个简单的s域例子，可以直接化简公式，然后直接输出公式的latex代码。

![[Omnivore/科研神器：Sympy推公式，无缝latex输出 - 知乎/attachments/2937eb2be14ad2a82b0e84eac5a3b28c_MD5.png]]

当然，Sympy的功能远远不止上面所展示的，还能积分、通分，进行拉普拉斯(逆)变换等。推荐一个用Sympy做工科相关计算的无敌教程，传送门如下：

## 小结

通过以上几个工具配合，Latex排版；Sympy推公式，输出公式的Latex语句，或者Mathpix Snipping生成公式代码识别输出代码。在熟练使用后，能极大提升工作流的效率。

\--------------------------------------------------- 

封面图片：Photo by [Hannah Lindahl](https://link.zhihu.com/?target=https%3A//unsplash.com/%40hannielindahl%3Futm%5Fsource%3Dunsplash%26utm%5Fmedium%3Dreferral%26utm%5Fcontent%3DcreditCopyText) on [Unsplash](https://link.zhihu.com/?target=https%3A//unsplash.com/t/current-events%3Futm%5Fsource%3Dunsplash%26utm%5Fmedium%3Dreferral%26utm%5Fcontent%3DcreditCopyText)

