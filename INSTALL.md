# Install Codex Micro Monitor Plugin

The complete plugin release includes the Micro application. After installing the plugin, ask Codex to open the Micro panel; a separate Store installation is not required. This package requires Windows x64, .NET 10 Desktop Runtime x64 and a signed-in Codex desktop client.

## Ask Codex to install it

Copy this into a Codex chat that can run commands on your Windows computer:

```text
Install Codex Micro Monitor Plugin 1.0.0 on this Windows x64 computer.
Use https://github.com/gantrol/codex-plugin-micro-keypad/releases/tag/v1.0.0.
Check that codex plugin add is available and .NET 10 Desktop Runtime x64 is installed.
Download codex-micro-monitor-plugin-1.0.0-win-x64.zip and SHA256SUMS.txt, then verify the ZIP checksum.
Extract the whole archive to a persistent directory under my user profile, preserving .agents/ and plugins/.
Inspect any existing installation before replacing files.
Run codex plugin marketplace add "<absolute extraction root>".
Run codex plugin add codex-micro-keypad@codex-micro-monitor.
Check the result with codex plugin list --marketplace codex-micro-monitor --json.
Report missing prerequisites if any, the installation path, and whether I need to restart the client manually.
This request only installs the plugin; do not send messages, stop turns or approve commands.
```

After restarting the desktop client and opening a new chat, ask:

> Use the Codex Micro Monitor plugin to read its capabilities and open the Micro panel.

Use the complete release ZIP. GitHub source archives and a Git checkout do not include the executable needed by the plugin's MCP server. The marketplace root is the directory containing `.agents/plugins/marketplace.json`, not the nested `plugins/codex-micro-keypad` directory.

## 中文安装引导

[完整中文引导：让 Codex 安装并打开 Micro 插件](https://github.com/gantrol/codex-micro-monitor/blob/main/docs/plugin-installation.zh-CN.md)，包含可直接复制的安装指令和手动命令。

安装后的完整插件已带有 Micro 程序。重启桌面客户端、新建聊天后，可以说：

> 请使用 Codex Micro Monitor 插件，先读取可用功能，再打开 Micro 面板。

该流程不会自动安装商店版或创建开始菜单入口。“先装轻量插件，再由插件下载并安装软件”需要独立安装技能和脚本，1.0.0 尚未实现。

The CLI syntax was checked with `codex-cli 0.160.0`. Older clients without `plugin add` can use the desktop plugin directory after registering the local marketplace; see the [official OpenAI local-marketplace guide](https://developers.openai.com/plugins/build/plugins#add-a-marketplace-from-the-cli). A fresh installation and live Codex acceptance have not yet been performed for this release.
