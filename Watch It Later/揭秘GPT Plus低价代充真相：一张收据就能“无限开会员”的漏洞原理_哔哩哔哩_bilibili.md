---
url: https://www.bilibili.com/video/BV1MrdsBoES6/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2026-05-01T18:10:10+08:00
---
![揭秘GPT Plus低价代充真相：一张收据就能“无限开会员”的漏洞原理_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1MrdsBoES6/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c)
揭秘GPT Plus低价代充真相：一张收据就能“无限开会员”的漏洞原理
https://www.bilibili.com/video/BV1MrdsBoES6/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
蔡沟的学习笔记 2026-04-19 05:10:15

跟大家说个关键事，咱们今天聊的g p t plus低价代充漏洞，是OpenAI官方社区有人爆料出来的，写这篇文就是帮大家避坑，别交智商税，这个漏洞没被修复，纯属OpenAI懒得管，说不定哪天就堵上了，到时候代充的钱就打水漂了，二手平台上那些十几20块的g p t plus代充，看着巨香，对不对，其实根本不是啥内部渠道，就是钻了OpenAI的IOS内购漏洞，操作特简单，全是灰色地带，先简单说下正常流程，app里点开通跳app store付钱，apple生成内购收据，存你手机app，再把收据和你账号的令牌打包发给OpenAI验证，通过就开通会员，重点来了，这个漏洞的核心的是OpenAI验证时偷了懒，只查两样东西，收据是不是apple官方生成的，需要保证没被篡改，账号令牌是不是有效的，账号有没有过期，账号退没退出，至于这张收据对应的apple id，和你要充的ChatGPT账号有没有绑定，他压根不管，举个好懂的例子，就好比你拿着别人的超市购物小票，去柜台领对应商品，柜员只核对小票是真的假的，既不看小票上的购买人是谁，也不查你的身份证，只要小票没问题，直接就把商品递给你，这里的小票就是apple内购收据，商品就是g p t plus会员代充，商家就是靠捡别人的小票，反复领商品赚钱，二手平台商家代充就四步，第一步搞一张低价收据，商家注册土耳其区apple id那边，g b t plus月费499里，拉折人民币85块左右。

比国内便宜一半，充好礼品卡付钱就能拿到一张合法收据，第二步拦截收据，别让它自动上报，付钱后，apple会把收据存手机，本地商家用工具拦截，不让ChatGPT app把收据发给OpenAI，不然收据会和临时账号绑死，没法反复用，第三步导出收据，这一步是关键，以下三种方法都不用高深技术，第一种端点本地映射，这种方法无需越狱，最主流用meant proxy，charles proxy这类代理工具，或者自建HTPS代理加自签证书，通过DNS劫持或本地代理，把ChatGPT app发往OpenAI的请求，重定向到自己的本地服务器，因为app发送的请求里，本身就带着base64编码的收据，转到本地后直接保存就能用，第二种越狱加hook，这种方法粗暴直接，如果有越狱的IPHONE，用freda flex这类工具，直接hook iOS的STOCKET框架，STOKIT框架是负责处理内购的系统框架，要么截获sk payment transaction的transaction，Receipt，也就是内购交易收据，要么直接读取手机本地的app store，receipt url收据文件路径就能轻松拿到收据，第三种安卓路径，安卓用户操作逻辑和第二种类似，用EXPOST框架进行hook拦截，ChatGPT安卓版的内购收据，原理和IOS越狱hook一致，只是工具和系统框架不同，操作也很简单，第四步，反复代充一本万利，让客户给账号令牌，把收据和令牌一起发给OpenAI验证通过，就开通会员，客户改完密码，令牌失效。

收据还能继续给下一个人，用一张85块的收据能充无数个账号，这就是低价代充的真相，OpenAI不修复，不是修不了，是个人plus订阅收入不值一提，但漏洞随时可能堵，到时候代充的会员可能被取消，账号还可能被封，最后劝一句，别贪便宜交智商税，低价代充违规还可能泄露隐私，不如走官方渠道，踏实又安全。



--- 由 vCaptions 生成 ---