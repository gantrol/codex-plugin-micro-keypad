# Codex Micro Monitor plugin

Windows plugin distribution for [Codex Micro Monitor](https://github.com/gantrol/codex-micro-monitor).

## Source ownership

The editable source of `plugins/codex-micro-keypad/`, `.agents/plugins/marketplace.json` and `LICENSE` lives in **codex-micro-monitor**. This repository mirrors those files for distribution; make plugin changes in the product repository first. This root README and repository instructions are maintained here. Runtime binaries are produced by the product's packaging scripts and distributed in release ZIPs.

Keep `codex-micro-monitor`, `codex-control` and `codex-plugin-micro-keypad` as sibling checkouts under `AgentTools/`. Use `AgentTools/` as the local Codex project's primary folder. From `codex-micro-monitor`, run:

```bash
python3 scripts/sync-plugin-source.py --check
python3 scripts/sync-plugin-source.py --apply
```

The check is read-only. Apply refuses to overwrite local changes in mirrored files and never commits, pushes or publishes. See the [repository map](https://github.com/gantrol/codex-micro-monitor/blob/main/docs/repository-layout.zh-CN.md). The distribution repository is not a build dependency of the desktop product.

## Install

- Download the complete plugin ZIP from [Releases](https://github.com/gantrol/codex-plugin-micro-keypad/releases/latest). It requires .NET 10 Desktop Runtime x64 and a signed-in Codex desktop app.
- Follow the [installation instructions](https://github.com/gantrol/codex-micro-monitor#install). Source archives do not contain `bin/CodexMicro.Plugin.exe`; use the release plugin ZIP.
- Product source, builds and shared panel changes belong in the [main product repository](https://github.com/gantrol/codex-micro-monitor), version 1.0.0 / Windows file version 1.0.0.0.
- [macOS development handoff](https://github.com/gantrol/codex-micro-monitor/blob/main/docs/architecture/macos-development-handoff.zh-CN.md): no macOS plugin is available yet.
- Public plugin-directory submission and live plugin-install acceptance remain pending.

Windows 插件分发仓库。请下载完整 Release 插件包；源码归主产品仓库维护。Microsoft Store 独立桌面版已发布：

<a href="https://apps.microsoft.com/detail/9NTVMG9QNMHC"><img src="https://get.microsoft.com/images/zh-cn%20dark.svg" alt="从 Microsoft Store 获取" width="200" /></a>

License: [GNU General Public License v3.0 only (GPL-3.0-only)](LICENSE).

Third-party visual rights are described in the [product notice](https://github.com/gantrol/codex-micro-monitor/blob/v1.0.0/README.md#notice).
