# Repository ownership

- This is the distribution repository for `codex-micro-monitor`.
- Edit plugin manifests, MCP configuration, skills and assets in the sibling product repository's `plugins/codex-micro-keypad/`, then use its `scripts/sync-plugin-source.py`.
- `.agents/plugins/marketplace.json` and `LICENSE` also mirror the product repository. Maintain this root README and repository instructions here.
- Do not add product implementation, project references, submodules, or runtime binaries here. Build release archives from the product repository.
- Do not use subagents. Do not add tests or run live UI tests unless explicitly requested by the user.
