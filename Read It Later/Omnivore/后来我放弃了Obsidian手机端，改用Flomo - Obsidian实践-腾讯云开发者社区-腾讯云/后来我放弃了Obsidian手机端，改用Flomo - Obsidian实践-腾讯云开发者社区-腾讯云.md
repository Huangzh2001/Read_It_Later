---
id: 0364d88f-886a-467c-9c55-5122731a0a2e

url: https://cloud.tencent.com/developer/article/2390893
status:
---


tags::  #Readed 

# 后来我放弃了Obsidian手机端，改用Flomo | Obsidian实践-腾讯云开发者社区-腾讯云
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-flomo-obsidian-1935dd0a528)
[Read Original](https://cloud.tencent.com/developer/article/2390893)

Obsidian在本地管理笔记文件的方式是把双刃剑。一方面，用户自行管理笔记文件可以获得更多的安全感，不用担心会出现“平台挂掉了，笔记丢失”的情况；另一方面，免费版Obsidian无法进行多终端笔记同步的问题又常常遭人诟病。

针对多终端笔记同步的问题，我们：

* 借助坚果云实现了Obsidian笔记在PC终端的同步：[如何实现Obsidian笔记云同步？| 实践](https://cloud.tencent.com/developer/tools/blog-entry?target=http%3A%2F%2Fmp.weixin.qq.com%2Fs%3F%5F%5Fbiz%3DMzU3OTM4OTkzNQ%3D%3D%26mid%3D2247486409%26idx%3D1%26sn%3Ddba56acef5e6d70837e588143266a7e2%26chksm%3Dfd679b49ca10125f02a163bd33b85921f7a32fc962315059fea84690fc2d4a8c341c25bbf232%26scene%3D21%23wechat%5Fredirect&objectId=2390893&objectType=1)；
* 借助FolderSync实现了Obsidian笔记在移动端的同步：[如何在手机端实现Obsidian笔记云同步 | Obsidian实践](https://cloud.tencent.com/developer/tools/blog-entry?target=http%3A%2F%2Fmp.weixin.qq.com%2Fs%3F%5F%5Fbiz%3DMzU3OTM4OTkzNQ%3D%3D%26mid%3D2247486867%26idx%3D1%26sn%3D246d0eeee7860c60237836c8b5166c35%26chksm%3Dfd679d13ca101405489c1750ea6d81f4bf352b3486b1ac72c0cd0b5b5e382892af55f4a9a381%26scene%3D21%23wechat%5Fredirect&objectId=2390893&objectType=1)。

经过一段时间的试用和磨合，最终，PC终端同步沿用至今，但移动端同步没过多久就放弃了，主要原因是：

**占用手机存储空间。**理论上，纯文本的Markdown笔记文件，不会占用很大存储空间，但架不住图片和参考资料多啊，以至于，只10个月的积累，同步整个Obsidian库就占用了2G+手机存储空间，这谁受得了？尤其是，这个规模还在飞速地增长。港真，对于手机而言，Obsidian实在是太重了——或许，平板电脑能稍好一些？

**需要手动执行同步。**一般使用笔记工具，希望打开笔记的一瞬间，即可获得最新；然而实际情况却是，直到使用笔记的那一个瞬间，才会想到要启动FolderSync进行同步。担心同步完成之前编写笔记，可能造成不必要的版本冲突；等到同步完成再去编辑笔记，基本上黄花菜也就凉了……

**内容同步云端失败。**尝试在Obsidian手机端编写内容，但是最终未能同步到PC端。跟踪整个同步的过程，从手机端到云端再到PC端，貌似是手机端到云端的同步失败了，但是最终没有找到解决办法——不知道你是否也遇到过这种情况，如果有好的解决方法，能否分享下？

当然还有一种可能是，其实我也并没有竭尽所能去寻找解决办法，单纯想要放弃了，因为，在手机端使用Obsidian好像也没有那么必要。

回想一下，我们使用手机的时候，更多地是浏览内容，而很少会去编写大篇幅的内容。即便是说，记录的需求是真实的，通常，也只是简短地记录灵感或者思路，便于后续回忆整理就可以了；像Obsidian的反向链接、关系谱图这种高级功能，则完全没有必要，也很难在手机的小屏幕上有很好的呈现效果——别问我是怎么知道。

于是，我决定放弃了Obsidian手机版，转而去物色一个好用的Memo工具，最好还可以支持多终端云同步，方便拷贝，不需要重复录入内容……最终，我选择了Flomo。

![](https://proxy-prod.omnivore-image-cache.app/0x0,slI_sPlKcu0-AhEVl3oQwxpfEx9Sid7yANJ0KdW2_Iso/https://developer.qcloudimg.com/http-save/yehe-2838019/2db9edec6e694f71aa5b90a1c26e28ad.png)

笔记管理逻辑

借用《卡片笔记写作法：如何实现从阅读到写作》的笔记管理逻辑（[卡片笔记，一个不断增长的外部思想库 | 读书](https://cloud.tencent.com/developer/tools/blog-entry?target=http%3A%2F%2Fmp.weixin.qq.com%2Fs%3F%5F%5Fbiz%3DMzU3OTM4OTkzNQ%3D%3D%26mid%3D2247486356%26idx%3D1%26sn%3D297df58067c736c2ba2bcbce42112dba%26chksm%3Dfd679b14ca101202789030aa1d2b8bbfa28c3ffcbe293d132d7b586aca6592a93704c7ec1be3%26scene%3D21%23wechat%5Fredirect&objectId=2390893&objectType=1)），来理解Flomo与Obisidian的协作关系：

* Flomo：记录闪念笔记；
* Obsidian：将闪念笔记整理为永久笔记，并进行管理。

![](https://proxy-prod.omnivore-image-cache.app/0x0,slWhMJdl3STa-c8O13ECwS2JRypKHK7b_tlPF67OIkMc/https://developer.qcloudimg.com/http-save/yehe-2838019/5cca2edf278719224d19f08cf682e61b.png)

操作逻辑

操作逻辑也非常简单：

* 在手机端：使用Flomo App编辑Memo，内容存储于Flomo云平台；
* 在电脑端：  
   * 使用flomo Web查看Memo；  
   * 使用Obisidian重新编辑Memo，并整理为笔记。

![](https://proxy-prod.omnivore-image-cache.app/0x0,s0misNqSyeCkcwN_7MABa3WBaTui7KfTTzYaRb-aqNlA/https://developer.qcloudimg.com/http-save/yehe-2838019/75b0effd1f87cd755232aba769df8f1d.png)

实践案例

举2个个人实践案例作为参考。

比如说，我在电影院观看电影《流浪地球II》时，使用手机端Flomo App将即时的感想，简短地记录为Memo：

![](https://proxy-prod.omnivore-image-cache.app/0x0,sX_dvZ61Jp5nmQzHlXLz_KuivVQLsuoeP3ne9ZLcU2P0/https://developer.qcloudimg.com/http-save/yehe-2838019/dffd50e81d07764ee51abb17c38f9ba4.jpg)

回到家后打开电脑，对照着Flomo Web记录的Memo，回顾观影时的想法，在Obisidian中整理为笔记：20230124 电影《流浪地球II》观后。

![](https://proxy-prod.omnivore-image-cache.app/0x0,stAQlAEGTvx5Tnks-KqBMHYtZn46SrRtKFCyQ_iQ88xs/https://developer.qcloudimg.com/http-save/yehe-2838019/15e72d7d62c5ee8d1a4295cc6dd509d3.png)

再比如说，杨康之后，我打算把自己从最开始检出10混1阳性，一直到后来免疫系统与奥密克戎的7日对决，做一个完整的记录。于是，利用上下班路上乘坐公共汽车的时间，我回忆并梳理了这段经历，并使用Flomo App进行了简短记录：

![](https://proxy-prod.omnivore-image-cache.app/0x0,sjPLWTX9v7Vm5r-0e3YAgUhiRz_C29p_c7Vm7gX31AA4/https://developer.qcloudimg.com/http-save/yehe-2838019/1382be983072d3d21db737e139425186.jpg)

在方便使用电脑的时候，对照着Flomo Web上呈现的记录，将可以复用的内容拷贝到Obsidian，并进一步扩写细节、感想，以及复盘总结等内容：2022-12-24 回顾小阳人的经历。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sYcxEYQlOEWNnNjf9K_lJRt7Je3xaMWpBLlMndI4dTj4/https://developer.qcloudimg.com/http-save/yehe-2838019/a5f7d549e5869725604f94356520bb50.png)

借助于Flomo的帮助，我可以轻松实现随时随地记录想法，不用担心灵感会一闪而过，再无法想起；而当想法一旦被记录下来，又可以心无旁骛地转头去做其他事情，不必时时上心记挂——犹如卸下了头脑的重负。

关于Flomo

Flomo（浮墨笔记）是一个非常小而美的知识管理应用，极简、优美又高效。创始团队在知识管理方面有着很深刻的见解，甚至众筹策划了一本书来传播构建知识资产的理念，可见其专注与野心。虽然我是Obsidian的重度用户，使用Flomo不过基本功能，浅尝辄止，却不时访问Flomo的官方网站，试图从“Flomo方法”中获得一些启发。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sd5tNmG6zB18O9fH9jFyYt9ZJmwkN1ZedqCWE-mVHrlw/https://developer.qcloudimg.com/http-save/yehe-2838019/9b2413066fa1ed7fd48c018e4e30bfca.png)

既然Flomo这么好，又支持多终端，为什么还要Flomo+Obisidian两头用？浅做3点对比：

| 存储方式 | Web存储              | 本地存储        |
| ---- | ------------------ | ----------- |
| 功能   | 极简                 | 支持插件扩展      |
| 费用   | 基本功能免费；扩展功能需购买付费会员 | 承诺对个人用户永久免费 |

我个人的选择是，使用Flomo免费功能，在手机端完成日常的Memo记录；高级功能还是全权交给Obsidian吧，毕竟，作为一只Obsidian重度用户和彩虹屁爱好者，绝不可以浪得虚名。

不过，如果你喜欢极简、优美又高效的知识管理工具，并且愿意为此买单，我还是非常乐于向你真诚推荐Flomo。

本文参与 [腾讯云自媒体同步曝光计划](https://cloud.tencent.com/developer/support-plan)，分享自微信公众号。

