# 更新日志（Changelog）

本文件记录 Cursor 完整汉化工具的版本变更与适配的 Cursor 版本。

格式参考 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)；版本号对应「适配的 Cursor 版本 + 文档/词典更新日期」。

---

## [2026-06-26] — 适配 Cursor `3.8.24`

- **适配版本**：Cursor `3.8.24`（内置 VS Code `1.105.1`），macOS 验证通过。
- **词典**：
  - `Core_Dictionary.json` 新增 `cursor_3_8_24_新增` 分区，补充钩子阻止提示、异步问题、MCP/插件/自动化、身份验证、团队管理等约 120 条界面词条。
  - `Pattern_Dictionary.json` 新增智能体异步问题、审查结果、网络域名审查等动态正则规则。
  - `Ad_Popup_Dictionary.json` 补充版本更新通知、Claude Code 导入、Multitask 推广等弹窗文案。
- **兼容性**：`3.8.x` 同系列小版本通常可直接复用，升级后重跑脚本即可。

## [2026-06-24] — 适配 Cursor `3.8.23`

- **适配版本**：Cursor `3.8.23`（内置 VS Code `1.105.1`），macOS 验证通过。
- **文档**：
  - README 新增「注意事项」与「版本历史」章节。
  - 补充 “Your Cursor installation appears to be corrupt” 提示的**根因说明**：本工具只注入 `workbench.html` 并同步 `product.json` 校验值，不修改 `workbench.desktop.main.js`，因此不会触发完整性校验失败；该提示通常由**其他直接 patch 主程序 JS 的汉化工具**引起。
  - `使用说明.md` 增补「注意事项」。
  - 翻译文档 `翻译文档.md` 文档版本升至 `1.0.2`，更新版本对照表与兼容性说明。
- **兼容性**：`3.8.x` 同系列小版本通常可直接复用，升级后重跑脚本即可。

## [2026-06-23] — 首次发布，适配 Cursor `3.8.11`

- 首个公开版本。
- **适配版本**：Cursor `3.8.11`（内置 VS Code `1.105.1`）。
- 双层汉化：官方简体中文语言包（VS Code 内核界面）+ 注入脚本与本地词典（Cursor 专有界面）。
- 提供 `启动汉化_Mac.sh` / `取消汉化_Mac.sh` 一键脚本，支持 `--restore` 还原。

---

## 版本对照速查

| 日期 | 适配 Cursor | 内置 VS Code | 官方语言包 VSIX |
| --- | --- | --- | --- |
| 2026-06-26 | `3.8.24` | `1.105.1` | `1.105.2025101509` |
| 2026-06-24 | `3.8.23` | `1.105.1` | `1.105.2025101509` |
| 2026-06-23 | `3.8.11` | `1.105.1` | `1.105.2025101509` |

> 验证方法：`/Applications/Cursor.app/Contents/Resources/app/package.json` → `version`（Cursor 版本）；同目录 `product.json` → `vscodeVersion`（VS Code 引擎版本）。
