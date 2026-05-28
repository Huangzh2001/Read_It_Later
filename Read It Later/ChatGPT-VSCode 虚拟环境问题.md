# VSCode 虚拟环境问题

**User:** Anonymous  
**Created:** 5/27/2026 21:22:42  
**Updated:** 5/28/2026 15:17:59  
**Exported:** 5/28/2026 15:21:22  
**Link:** [https://chatgpt.com/g/g-p-691ed14bafb8819180399fafb246a46f/c/6a16eff8-4758-83a7-809e-b5e1a7269916](https://chatgpt.com/g/g-p-691ed14bafb8819180399fafb246a46f/c/6a16eff8-4758-83a7-809e-b5e1a7269916)  

## Response:
2026/5/28 15:17:27

下面整理成一个以后可复用的 **VS Code + Anaconda/Jupyter 卡死软修复方案**。这个方案的核心是：**不重装、不删除虚拟环境、不删除项目，只清理 VS Code/Jupyter 的残留状态，并重新绑定已有虚拟环境。**

---

# 一、这个方法适用于什么情况

适用于下面这种典型情况：

```text
1. VS Code 里运行 Python / Jupyter notebook 没有正常结束；
2. 直接关闭 VS Code 后，下次打开能扫描到虚拟环境，但加载不上；
3. Notebook 右上角 kernel 一直转圈、选不上、启动失败；
4. conda activate 环境名 可能卡住；
5. Anaconda Navigator 可能打不开；
6. 但是直接调用虚拟环境里的 python.exe 可以运行脚本。
```

你这次的情况就是：

```text
D:\Software\anaconda3\envs\LARP\python.exe 可以直接运行脚本
```

说明 **LARP 虚拟环境本身没有坏**。问题更可能出在：

```text
VS Code 残留状态
Jupyter kernel 残留进程
VS Code 的 Python/Jupyter 缓存
旧 workspace 绑定
conda 激活链路被卡住
```

---

# 二、安全修复命令：PowerShell 版

## 0. 操作前准备

先手动关闭：

```text
VS Code
Anaconda Navigator
Jupyter notebook / lab
CMD / PowerShell 中正在卡住的窗口
```

然后打开：

```text
管理员 PowerShell
```

---

## 1. 杀掉残留进程

```powershell
Stop-Process -Name Code -Force -ErrorAction SilentlyContinue
Stop-Process -Name python -Force -ErrorAction SilentlyContinue
Stop-Process -Name pythonw -Force -ErrorAction SilentlyContinue
Stop-Process -Name jupyter -Force -ErrorAction SilentlyContinue
Stop-Process -Name conda -Force -ErrorAction SilentlyContinue
Stop-Process -Name anaconda-navigator -Force -ErrorAction SilentlyContinue
Stop-Process -Name node -Force -ErrorAction SilentlyContinue
```

然后检查是否还有残留：

```powershell
Get-Process Code,python,pythonw,jupyter,conda,node,anaconda-navigator -ErrorAction SilentlyContinue
```

如果还有输出，再执行一次上面的 `Stop-Process`。

---

## 2. 备份 VS Code 的状态缓存

注意：这里是**改名备份**，不是删除。

```powershell
$CodeUser = "$env:APPDATA\Code\User"
$Stamp = Get-Date -Format "yyyyMMdd_HHmmss"

$Targets = @(
    "$CodeUser\globalStorage",
    "$CodeUser\History",
    "$CodeUser\workspaceStorage"
)

foreach ($Path in $Targets) {
    if (Test-Path -LiteralPath $Path) {
        Rename-Item -LiteralPath $Path -NewName "$(Split-Path $Path -Leaf).bak_$Stamp" -Force
        Write-Host "Backed up $Path"
    } else {
        Write-Host "Skip $Path"
    }
}
```

这一步会让 VS Code 忘掉一部分旧状态，包括：

```text
旧 workspace 状态
旧 notebook/kernel 状态
Python/Jupyter 扩展的部分缓存
窗口历史记录
```

不会删除：

```text
项目代码
虚拟环境
Anaconda
VS Code 软件本体
```

---

## 3. 重新注册 LARP 的 Jupyter kernel

```powershell
& "D:\Software\anaconda3\envs\LARP\python.exe" -m ipykernel install --user --name LARP --display-name "Python (LARP)"
```

如果输出类似：

```text
Installed kernelspec LARP in C:\Users\黄梓航\AppData\Roaming\jupyter\kernels\larp
```

说明 kernel 注册成功。你前面日志里确实已经出现过这个成功信息。`粘贴的文本 (1).txt`

---

## 4. 用命令打开 VS Code 项目

不要双击 `.ipynb` 文件打开。用 PowerShell 启动：

```powershell
code --disable-workspace-trust "D:\Document\中山大学-文件\不同步的大文件\LineagePert_Archive"
```

进入 VS Code 后：

```text
Ctrl + Shift + P
→ Python: Select Interpreter
→ Enter interpreter path
→ D:\Software\anaconda3\envs\LARP\python.exe
```

然后打开 notebook，右上角：

```text
Select Kernel
→ Python (LARP)
```

如果出现多个 `Python (LARP)`，选择路径指向这个的：

```text
D:\Software\anaconda3\envs\LARP\python.exe
```

---

# 三、完整可复制版本

以后再次遇到同类问题，可以直接用下面这整段：

```powershell
# ============================================================
# VS Code + Anaconda/Jupyter 软修复方案
# 不重装、不删环境、不删项目
# ============================================================

# 1. 杀掉残留进程
Stop-Process -Name Code -Force -ErrorAction SilentlyContinue
Stop-Process -Name python -Force -ErrorAction SilentlyContinue
Stop-Process -Name pythonw -Force -ErrorAction SilentlyContinue
Stop-Process -Name jupyter -Force -ErrorAction SilentlyContinue
Stop-Process -Name conda -Force -ErrorAction SilentlyContinue
Stop-Process -Name anaconda-navigator -Force -ErrorAction SilentlyContinue
Stop-Process -Name node -Force -ErrorAction SilentlyContinue

# 2. 备份 VS Code 用户状态缓存
$CodeUser = "$env:APPDATA\Code\User"
$Stamp = Get-Date -Format "yyyyMMdd_HHmmss"

$Targets = @(
    "$CodeUser\globalStorage",
    "$CodeUser\History",
    "$CodeUser\workspaceStorage"
)

foreach ($Path in $Targets) {
    if (Test-Path -LiteralPath $Path) {
        Rename-Item -LiteralPath $Path -NewName "$(Split-Path $Path -Leaf).bak_$Stamp" -Force
        Write-Host "Backed up $Path"
    } else {
        Write-Host "Skip $Path"
    }
}

# 3. 重新注册 LARP kernel
& "D:\Software\anaconda3\envs\LARP\python.exe" -m ipykernel install --user --name LARP --display-name "Python (LARP)"

# 4. 打开项目
code --disable-workspace-trust "D:\Document\中山大学-文件\不同步的大文件\LineagePert_Archive"
```

打开 VS Code 后再手动选择：

```text
Python: Select Interpreter
→ Enter interpreter path
→ D:\Software\anaconda3\envs\LARP\python.exe

Notebook:
Select Kernel
→ Python (LARP)
```

---

# 四、这次问题可能的原因

根据你这次的现象，最合理的解释是：

## 1. VS Code/Jupyter 没有正常释放 kernel 进程

你是在 VS Code 运行过程中直接关闭软件。Notebook kernel、Python 子进程、Jupyter 子进程可能没有正常退出，于是残留了多个：

```text
python.exe
pythonw.exe
jupyter.exe
node.exe
conda.exe
```

这些残留进程会影响下次启动 kernel。

---

## 2. VS Code 能扫描到环境，但启动 kernel 失败

VS Code 扫描到环境和真正启动 notebook kernel 是两回事：

```text
扫描到 LARP
≠ 成功启动 LARP kernel
```

你遇到的是：

```text
环境能看到
但是加载不上
```

这说明环境发现阶段可能成功，但 kernel 启动阶段失败。

---

## 3. conda 激活链路可能被卡住

这次你遇到：

```text
conda activate LARP 卡住
conda clean --lock 也卡住
```

所以 VS Code 如果内部尝试通过 conda 去激活 LARP，就会一起卡住。

但是：

```text
D:\Software\anaconda3\envs\LARP\python.exe 能直接运行
```

这说明不是 LARP 坏，而是 conda 管理层或 VS Code 调用 conda 的链路异常。

---

## 4. VS Code 的旧 workspace/kernel 状态污染

VS Code 会记住：

```text
上次使用的解释器
上次 notebook kernel
workspace 状态
Jupyter 连接状态
扩展状态
```

如果上次关闭时状态异常，下次可能继续读取坏状态。所以这次有效的关键步骤是：

```text
备份 globalStorage / workspaceStorage / History
```

让 VS Code 不再沿用旧的错误状态。

---

# 五、以后怎么避免复发

以后 notebook 没跑完时，尽量不要直接关 VS Code。先在 notebook 里执行：

```text
Interrupt
```

或者：

```text
Restart Kernel
```

或者：

```text
Shut Down Kernel
```

然后再关闭 VS Code。

如果必须强关 VS Code，下次出现：

```text
能看到环境，但 kernel 加载不上
```

就直接用上面的软修复流程，不要一开始就重装 Anaconda 或重建环境。



---
Powered by [ChatGPT Exporter](https://www.chatgptexporter.com)