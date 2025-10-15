---
date: 2025-10-15T16:52:47+08:00
url: https://www.bilibili.com/opus/1037333442111471639
status: readed
---
B站bilibili批量删除全部动态

![[Read It Later/attachments/0d5f4d1f876d1e34bca6f8e159c47360_MD5.webp]]

AmingX

2025年02月24日 09:43

很久之前搞得天选自动抽奖，今天发现转发了好多内容，几百几千条，一个个删属实费劲，所以写个脚本批量自动删除。

操作步骤：

1.电脑打开b站，登录后打开动态页面，按F12打开控制台，切换到console/控制台标签页，

2.复制以下代码粘贴进去 按回车即可

***注：该操作会删除全部动态，如果执行过程中需要终止，按F5刷新网页即可***

(async () => {

const sleep = (*ms*) => new Promise(*resolve* \=> setTimeout(resolve, *ms* \* 1000)); var data = document.querySelectorAll('.tp.bili-dyn-more\_\_btn'); console.log('当前数量:', data.length); const hoverEvent = new MouseEvent('mouseenter'); let i = 0; while (i < data.length) { const x = data\[i\]; x.dispatchEvent(hoverEvent); await sleep(0.5); console.log('正在删除第', i + 1, '个'); document.querySelectorAll('.bili-cascader-options\_\_item-custom')\[1\].click(); await sleep(0.5); document.querySelector('.bili-modal\_\_button.confirm.red').click(); await sleep(0.5); if (data.length - i < 5) { window.scrollBy(0, 100000); await sleep(0.5); data = document.querySelectorAll('.tp.bili-dyn-more\_\_btn'); console.log('重新获取，当前数量:', data.length); window.scrollBy(0, -100000); if (data.length) { i = 0; } else { console.log('已删除全部动态'); return; } } else { i++; } } })();

![[Read It Later/attachments/66aab5ddf03c3a537f2e135d764cf506_MD5.avif]]

注：该方法可能会随着B站网页更新而失效，2025.02.24测试有效

投诉或建议

⚠️ 无法加载数据