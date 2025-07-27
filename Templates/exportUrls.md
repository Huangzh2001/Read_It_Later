<%*
const now = new Date();
const pad = n => n.toString().padStart(2, '0');
const timestamp = `${now.getFullYear()}-${pad(now.getMonth()+1)}-${pad(now.getDate())}_${pad(now.getHours())}-${pad(now.getMinutes())}-${pad(now.getSeconds())}`;

const logFolderPath = 'utils/obsidian-urls/logs';

// 确保日志文件夹存在（递归创建）
async function ensureFolder(path) {
  if (!app.vault.getAbstractFileByPath(path)) {
    await app.vault.createFolder(path);
  }
}

await ensureFolder('utils');
await ensureFolder('utils/obsidian-urls');
await ensureFolder(logFolderPath);

const logFilePath = `${logFolderPath}/${timestamp}.md`;

async function appendLog(text) {
  let existing = '';
  const file = app.vault.getAbstractFileByPath(logFilePath);
  if (file) {
    existing = await app.vault.read(file);
  }
  await app.vault.modify(file || await app.vault.create(logFilePath, ''), existing + text + '\n');
}

// 记录开始
await appendLog(`# 导出日志\n- 时间: ${now.toLocaleString()}\n`);

// Step 1: 获取所有Markdown文件
const files = app.vault.getMarkdownFiles();
await appendLog(`- 读取Markdown文件数: ${files.length}`);

let urls = [];
let error = null;

try {
  for (const file of files) {
    const content = await app.vault.read(file);
    const match = content.match(/^url:\s*(.+)$/m);
    if (match) {
      const url = match[1].trim();
      if (!urls.includes(url)) urls.push(url);
    }
  }
  await appendLog(`- 提取到的URL数量: ${urls.length}`);

  // 确保目标文件夹存在
  const urlsFolderPath = 'utils/obsidian-urls';
  await ensureFolder(urlsFolderPath);

  // 写入 JSON 文件
  const jsonContent = JSON.stringify(urls, null, 2);
  const jsonFilePath = `${urlsFolderPath}/urls.json`;
  const existingJsonFile = app.vault.getAbstractFileByPath(jsonFilePath);
  if (existingJsonFile) {
    await app.vault.delete(existingJsonFile);
    await appendLog(`- 删除了旧文件 ${jsonFilePath}`);
  }
  await app.vault.create(jsonFilePath, jsonContent);
  await appendLog(`- 成功写入文件: ${jsonFilePath}`);

} catch(e) {
  error = e.message;
  await appendLog(`- 出错: ${error}`);
}

// 结束状态写入
await appendLog(error ? `- 状态: 失败` : `- 状态: 成功`);

%>
