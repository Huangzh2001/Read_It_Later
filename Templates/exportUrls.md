<%*
const now = new Date();
const pad = n => n.toString().padStart(2, '0');
const timestamp = `${now.getFullYear()}-${pad(now.getMonth()+1)}-${pad(now.getDate())}_${pad(now.getHours())}-${pad(now.getMinutes())}-${pad(now.getSeconds())}`;

const logFolderPath = 'utils/obsidian-urls/logs';

// 创建目录
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

// 日志头
await appendLog(`# Export Log\n- Time: ${now.toLocaleString()}\n`);

const files = app.vault.getMarkdownFiles();
await appendLog(`- Markdown files found: ${files.length}`);

let urlEntries = [];
let error = null;

try {
  for (const file of files) {
    const content = await app.vault.read(file);
    const urlMatch = content.match(/^url:\s*(.+)$/m);
    const statusMatch = content.match(/^status:\s*(.+)$/m);

    if (urlMatch) {
      const url = urlMatch[1].replace(/^"+|"+$/g, '').trim();
      const rawStatus = statusMatch ? statusMatch[1].trim().toLowerCase() : '';
      let statusLabel = 'unread';

      if (rawStatus === 'readed') statusLabel = 'read';
      else if (rawStatus === 'reading') statusLabel = 'reading';

      if (!urlEntries.find(e => e.url === url)) {
        urlEntries.push({ url, status: statusLabel });
      }
    }
  }

  await appendLog(`- URLs extracted: ${urlEntries.length}`);

  const urlsFolderPath = 'utils/obsidian-urls';
  await ensureFolder(urlsFolderPath);

  const jsonFilePath = `${urlsFolderPath}/urls-with-status.json`;
  const existingJsonFile = app.vault.getAbstractFileByPath(jsonFilePath);
  if (existingJsonFile) {
    await app.vault.delete(existingJsonFile);
    await appendLog(`- Deleted old file: ${jsonFilePath}`);
  }

  await app.vault.create(jsonFilePath, JSON.stringify(urlEntries, null, 2));
  await appendLog(`- Wrote new file: ${jsonFilePath}`);

} catch (e) {
  error = e.message;
  await appendLog(`- Error: ${error}`);
}

await appendLog(error ? `- Status: FAILED` : `- Status: SUCCESS`);
%>