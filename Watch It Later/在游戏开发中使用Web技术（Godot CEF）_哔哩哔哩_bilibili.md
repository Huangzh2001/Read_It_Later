---
url: https://www.bilibili.com/video/BV1BK67BCELg/?vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2026-04-03T13:51:11+08:00
---
![在游戏开发中使用Web技术（Godot CEF）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1BK67BCELg/?vd_source=06168f390bae49c4867767c52a20e87c)
在游戏开发中使用Web技术（Godot CEF）
https://www.bilibili.com/video/BV1BK67BCELg/?vd_source=06168f390bae49c4867767c52a20e87c
神楽坂minori 2026-01-28 13:34:20

如果你能在 Godot 游戏里运行一个功能齐全的网页浏览器会怎样？—— 有 GPU 加速、平滑的 120 FPS 渲染、并且完全可交互？不是作为覆盖层，而是作为一个实际的贴图，可以放在 3D 物体上，弯曲、扭曲并与之交互？，这就是 Godot CEF —— 一个为 Godot 引擎打造的高性能 Chromium 集成，使用 Rust 编写。，游戏 UI 开发不容易。用游戏引擎自带的节点去构建复杂、响应迅速、有动画的界面很耗时。而网页开发者有几十年的工具链 —— HTML、CSS、JavaScript、React、Vue —— 用来做漂亮、交互丰富的界面。，如果你能在 Godot 里用这些网页技能怎么办？以前有一些解决方案，但都有局限：纯软件渲染太慢，系统原生的 webview 不能嵌入 3D 场景，跨平台一致性也是一场噩梦。，我们打造 Godot CEF，就是为了解决这个问题。，Godot CEF 是针对 Godot Engine 4.5 及以上的高性能 Chromium Embedded Framework 集成。它完全用 Rust（基于 godot-rust）编写，带来内存安全和现代化工具链。，核心是一个强大的节点：CefTexture。该节点把任意网页内容 —— HTML、CSS、JavaScript、WebGL，甚至 WebGPU —— 直接渲染成 Godot 贴图。，使用非常简单。，看——只要四行代码。就这么简单。，最重要的特性是 GPU 加速的离屏渲染。在 Windows 上我们支持 DirectX 12。

在 macOS 上支持 Metal。在 Linux 和 Windows 上支持 Vulkan。网页内容直接在 GPU 上渲染，能达到嵌入式浏览器从未有过的帧率。，因为 CefTexture 渲染为真实的 Godot 贴图，你可以把它用在任何地方 —— 2D 画布、3D 网格、弯曲表面的材质。想在游戏里的电视屏幕上放一个浏览器？没问题。想在 VR 里做一个全息 UI？当然可以。，Godot 和 JavaScript 可以无缝互通。在 GDScript 里用 eval() 执行 JavaScript，并通过我们的 IPC 系统把消息发回 Godot。延迟在一帧范围内，适合用 Vue 或 React 等网页框架来做游戏 UI。，这不是某个受限的 webview。这是 Chromium —— 和 Google Chrome 同样的引擎。现代 JavaScript、HTML5、CSS3、WebGL、WebGPU —— 都能正常工作。我们通常启动 vite 开发服务器，实时热重载并交互式编辑 UI，非常方便。，我们还包含了 Chrome DevTools 的远程调试支持。检查元素、调试 JavaScript、性能分析 —— 都像你习惯的那样可用。，说到一个看似简单却让我调试了好几周的问题：多 GPU 系统。，现代笔记本通常有两块 GPU —— 为续航用的集成 Intel/AMD GPU，和为性能用的独立 NVIDIA/AMD GPU。当 Godot 和 CEF 需要共享贴图时，它们必须使用同一块 GPU。跨 GPU 的贴图共享是不存在的。。

如果没有明确协调，Godot 可能会为了性能选择独立 GPU，而 CEF 的子进程默认用集成 GPU。贴图句柄在创建它的 GPU 上是有效的，其他 GPU 上则无效。，我们的解决方案？GPU 设备锁定（device pinning）。，启动时，我们查询 Godot 的 RenderingDevice，获取 GPU 厂商和设备 ID。在 Windows 的 DirectX 下，就是 DXGI Adapter 描述。在 Vulkan 下就是 VkPhysicalDeviceProperties。在 macOS 的 Metal 下，我们会深入 IOKit Registry。，然后把这些 ID 作为命令行开关传给每个 CEF 子进程。Chromium 会用这些 ID 来选择完全相同的 GPU 适配器。，这是个简单的解决办法，但发现它需要理解 Godot 和 Chromium 的 GPU 进程选择架构。例如，你必须以十进制格式把 ID 传给 CEF，而它们通常以十六进制表示。，现在说一件让我夜不能寐的事：Vulkan 扩展注入。GPU 加速的贴图共享需要特定的 Vulkan 扩展。在 Windows 上是 VK_KHR_external_memory_win32。在 Linux 上是 VK_KHR_external_memory_fd 和 VK_EXT_external_memory_dma_buf。这些扩展允许一个进程导出贴图句柄，另一个进程导入它。，问题是：Godot 并没有启用这些扩展。当 Godot 创建 Vulkan 设备时，它只请求内部需要的扩展。

GDExtensions 没有 API 能说 “嘿，我需要这些额外的扩展”。，当引擎不给你 API 时你怎么办？你就自己造一个。，我们使用运行时函数钩取（function hooking）。具体来说，我们钩取 vkCreateDevice —— 创建逻辑设备的 Vulkan 函数。，时机很关键。钩子必须在 Godot 创建 Vulkan 设备之前安装。我们仔细阅读了 Godot 源码，发现可以在 GDExtension 的 Core 初始化阶段安装 —— 这是能做到的最早时点。，这做法是否有点 hack？绝对。稳定吗？出乎意料地还行。杀毒软件会不会报？可能会。，但问题是——我们不满足于这些变通办法。我们已经向上游提交了两个贡献，来完全消除这些 hack 的必要性。，首先，向 retour-rs 提交的 PR #77，为函数钩取添加了 ARM64 支持。其次，也是关键的，向 Godot 本体提交的 PR #114940。它为 GDExtensions 在设备创建阶段请求额外的 Vulkan 扩展添加了正式 API。，一旦 Godot 合并了这个 PR，整个基于钩子的做法就不再需要了。GDExtensions 将能通过官方 API 干净地请求 VK_KHR_external_memory 等扩展。在此之前，钩子还能用。但我们正积极让它们变得多余。，最好的代码是你最终可以删除的代码。，你可能会问——我们给 retour 添加了 ARM64 支持，为什么 Vulkan 钩取在 macOS 上不起作用？

答案是：根本没有可钩取的点。，Godot 把 MoltenVK（Vulkan 到 Metal 的翻译层）静态链接进了二进制。当 Godot 调用 vkCreateDevice 时，并不是通过动态库的 PLT 或 GOT 表去调用，而是直接跳转到嵌入的代码。没有给我们拦截的间接点。，函数钩取是通过替换这些间接表中的条目来实现的。没有表？就没法钩取。就是这么简单。，我们在 retour 上花了几周做 ARM64 支持，然后意识到……对 macOS 并无意义。入口点就是不存在。，但有好消息：我们不需要它。macOS 原生支持 Metal，而且 Metal 的 IOSurface 共享工作得很漂亮 —— 不需要任何 hack。实际上这是我们实现得最干净的平台。，这个项目不是在真空中诞生的。它是在开发 Engram 时创建的，Engram 是一个需要复杂交互式 UI 的 CRPG 游戏。，最初的版本使用 godot_wry，对于覆盖层 UI 很好用。但我们需要更多 —— 在 Linux 上表现不好，跨平台一致性差。大约 50% 的启动崩溃是因为用户在用没有内置 Edge webview 的旧 Windows 版本。，所以我们构建了 Godot CEF。现在我们把它开源给整个 Godot 社区。，公平地说 —— Godot CEF 并不是唯一的选择。godot_wry 使用操作系统原生的 webview。它轻量且适合简单覆盖层，但浏览器是叠加在游戏之上的，无法嵌入 3D 场景，且各平台行为不同。

gdcef 是基于 CEF 的 C++ 集成，历史更久，但它只做软件渲染，性能受限。Godot CEF 给你两全其美：GPU 加速带来性能，基于贴图的渲染带来灵活性，统一的 Chromium 引擎带来一致性。，开始很简单。去 Godot 资产商店或我们的 GitHub releases 页面，下载各平台的预构建二进制，解压到你项目的 addons 文件夹。，完整的 API 文档在线可查，涵盖属性、方法、信号，以及拖放和输入法支持等高级功能。如果你想从源码构建，我们也提供说明。项目使用 Rust nightly，我们的 xtask 构建系统处理打包 CEF 二进制的所有复杂性。，Godot CEF 是开源的，采用 MIT 许可。如果这个项目对你有用，考虑在 GitHub 上给我们点个星 —— 这能帮助更多人发现项目。我们欢迎贡献！无论是 bug 报告、功能请求，还是 pull request —— 请查看我们的贡献指南参与进来。如果你想帮助让 Godot 对大家更好 —— 不只是 Godot CEF 的用户 —— 可以考虑在我们的 Godot PR #114940 下留下支持性评论。社区支持有助于 PR 更快被评审和合并。，如果你用 Godot CEF 做出什么很酷的东西，我们很想看到。@我们、分享你的作品，让我们一起推动 Godot 的可能性边界。，谢谢收看。



--- 由 vCaptions 生成 ---