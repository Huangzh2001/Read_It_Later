---
created: 星期日, 十一月 24日 2024, 10:27:51 晚上
updated: 星期日, 七月 6日 2025, 4:31:48 下午
---
# Flomo 未归档文件

```dataviewjs
// 获取所有文件并过滤掉包含 #Archived 的文件
let pages = dv.pages('"Clippings/Flomo/memos"') // 指定文件夹路径

// 异步处理每个文件
await Promise.all(pages.map(async (page) => {
    // 使用 dv.io.load 异步读取文件内容
    const content = await dv.io.load(page.file.path);
    
    // 如果正文中不包含 #Archived，展示文件信息
    if (!content.includes("#Archived")) {
        dv.header(3, page.file.link); // 显示文件标题
        dv.paragraph(content || "没有内容"); // 显示文件内容，如果没有内容则显示 "没有内容"
    }
}));
```
