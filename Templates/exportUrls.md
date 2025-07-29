<%*
const maxChars = 1000;  // 摘要最大字数

// 限制字数的摘要提取函数
function extractExcerpt(text, maxChars) {
  let excerpt = '';
  const paras = text.split(/\n\s*\n/).filter(p => p.trim().length > 0);

  for (const p of paras) {
    if ((excerpt + p).length > maxChars) {
      excerpt += p.slice(0, maxChars - excerpt.length);
      break;
    } else {
      excerpt += (excerpt ? '\n\n' : '') + p;
    }
  }
  return excerpt;
}

// 创建目录辅助函数
async function ensureFolder(path) {
  if (!app.vault.getAbstractFileByPath(path)) {
    await app.vault.createFolder(path);
  }
}

const now = new Date();
const pad = n => n.toString().padStart(2, '0');
const timestamp = `${now.getFullYear()}-${pad(now.getMonth()+1)}-${pad(now.getDate())}_${pad(now.getHours())}-${pad(now.getMinutes())}-${pad(now.getSeconds())}`;

const logFolderPath = 'utils/obsidian-urls/logs';
await ensureFolder('utils');
await ensureFolder('utils/obsidian-urls');
await ensureFolder(logFolderPath);

const logFilePath = `${logFolderPath}/${timestamp}.md`;
async function appendLog(text) {
  let existing = '';
  const file = app.vault.getAbstractFileByPath(logFilePath);
  if (file) existing = await app.vault.read(file);
  await app.vault.modify(file || await app.vault.create(logFilePath, ''), existing + text + '\n');
}

await appendLog(`# 导出日志\n- 时间: ${now.toLocaleString()}\n`);

// 取所有 Markdown 文件
const files = app.vault.getMarkdownFiles();
await appendLog(`- 读取Markdown文件数: ${files.length}`);

let noteEntries = [];
let error = null;

try {
  for (const file of files) {
    const content = await app.vault.read(file);
    // 找 url
    const urlMatch = content.match(/^url:\s*(.+)$/m);
    if (!urlMatch) continue;
    const url = urlMatch[1].replace(/^"+|"+$/g, '').trim();

    // 笔记名
    const noteTitle = file.basename;

    // 摘要：去掉 YAML 头和 url 等字段，取正文前三段或 100 字以内
    // 先去掉 YAML frontmatter
    let body = content.replace(/^---[\s\S]*?---/, '').trim();

    // 去除 url、status 等元信息行
    body = body.split('\n').filter(line => !line.match(/^(url|status|date|tags):\s*/i)).join('\n').trim();

    const excerpt = extractExcerpt(body, maxChars);

    noteEntries.push({ noteTitle, url, excerpt });
  }

  await appendLog(`- 笔记条目数: ${noteEntries.length}`);

  // 写 JSON 文件
  const urlsFolderPath = 'utils/obsidian-urls';
  await ensureFolder(urlsFolderPath);

  const jsonFilePath = `${urlsFolderPath}/notes-with-excerpt.json`;
  const existingJsonFile = app.vault.getAbstractFileByPath(jsonFilePath);
  if (existingJsonFile) {
    await app.vault.delete(existingJsonFile);
    await appendLog(`- 删除旧文件: ${jsonFilePath}`);
  }

  await app.vault.create(jsonFilePath, JSON.stringify(noteEntries, null, 2));
  await appendLog(`- 写入新文件: ${jsonFilePath}`);

} catch(e) {
  error = e.message;
  await appendLog(`- 出错: ${error}`);
}

await appendLog(error ? '- 状态: 失败' : '- 状态: 成功');
%>
