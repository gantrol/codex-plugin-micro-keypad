# Codex Micro Monitor plugin

Windows plugin distribution for [Codex Micro Monitor](https://github.com/gantrol/codex-micro-monitor).

## Install

Send this to Codex:

> Please install this plugin: https://github.com/gantrol/codex-plugin-micro-keypad
> Use the complete plugin package from the latest Release, check the runtime requirements, and finish installation.

After installation, restart Codex when prompted, open a new chat, and say:

> Open Micro.

The plugin already includes Micro; no separate desktop installation is needed. Currently supported on Windows x64.

- Product source, builds and shared panel changes belong in the [main product repository](https://github.com/gantrol/codex-micro-monitor), version 1.0.0 / Windows file version 1.0.0.0.
- [macOS development handoff](https://github.com/gantrol/codex-micro-monitor/blob/main/docs/architecture/macos-development-handoff.zh-CN.md): no macOS plugin is available yet.
- Public plugin-directory submission and live plugin-install acceptance remain pending.

The standalone desktop app is also available on [Microsoft Store](https://apps.microsoft.com/detail/9NTVMG9QNMHC).

License: [GNU General Public License v3.0 only (GPL-3.0-only)](LICENSE).

Third-party visual rights are described in the [product notice](https://github.com/gantrol/codex-micro-monitor/blob/v1.0.0/README.md#notice).

## Source ownership

The editable source of `plugins/codex-micro-keypad/`, `.agents/plugins/marketplace.json` and `LICENSE` lives in **codex-micro-monitor**. This repository mirrors those files for distribution; make plugin changes in the product repository first. This root README and repository instructions are maintained here. Runtime binaries are produced by the product's packaging scripts and distributed in release ZIPs.

Keep `codex-micro-monitor`, `codex-control` and `codex-plugin-micro-keypad` as sibling checkouts under `AgentTools/`. Use `AgentTools/` as the local Codex project's primary folder. From `codex-micro-monitor`, run:

```bash
python3 scripts/sync-plugin-source.py --check
python3 scripts/sync-plugin-source.py --apply
```

The check is read-only. Apply refuses to overwrite local changes in mirrored files and never commits, pushes or publishes. See the [repository map](https://github.com/gantrol/codex-micro-monitor/blob/main/docs/repository-layout.zh-CN.md). The distribution repository is not a build dependency of the desktop product.

---

## 简体中文

### 安装

把下面这段发给 Codex：

> 请帮我安装这个插件：https://github.com/gantrol/codex-plugin-micro-keypad
> 使用最新 Release 中的完整插件包，检查运行环境并完成安装。

安装完成后，按提示重启 Codex，新开聊天说：

> 打开 Micro。

插件已包含 Micro 程序，无需另外安装桌面版。目前支持 Windows x64。

Windows 插件分发仓库。请下载完整 Release 插件包；源码归主产品仓库维护。Microsoft Store 独立桌面版已发布：

<a href="https://apps.microsoft.com/detail/9NTVMG9QNMHC"><img src="https://get.microsoft.com/images/zh-cn%20dark.svg" alt="从 Microsoft Store 获取" width="200" /></a>

许可：[GNU GPL v3.0 only（GPL-3.0-only）](LICENSE)。第三方视觉权利参见[项目声明](https://github.com/gantrol/codex-micro-monitor/blob/v1.0.0/README.md#notice)。
