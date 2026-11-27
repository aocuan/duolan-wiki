---
title: agent-browser
type: 项目卡
tags:
  - 开源项目
  - 浏览器
  - 工具
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/vercel-labs/agent-browser
  - https://agent-browser.dev
publish: true
repo: https://github.com/vercel-labs/agent-browser
license: Apache-2.0
stars: 54221
verdict: 给 agent 用的命令行浏览器：每步一条短命令、读无障碍树快照；比整页截图省上下文
---

# agent-browser

[agent-browser](https://github.com/vercel-labs/agent-browser) 是 Vercel Labs 用 Rust 写的浏览器自动化命令行工具。agent 每次执行一条短命令：`snapshot` 把页面变成紧凑的无障碍树文本，每个可操作元素带一个 `@e1` 这样的引用；agent 对引用点击或输入，再重新读页面确认结果。浏览器在命令之间保持打开。许可证 Apache-2.0，星标 54,221，截至 2026-11-26（太平洋时间）。

## 判断

它代表一种越来越常见的做法：不让模型看截图、也不写一整段脚本，而是让 agent 用 shell 一步步操作，每步只拿到很小的文本。和 [[Agentic搜索]] 的思路相同，都是把工具做成 agent 在循环里反复调用的小命令。

## 和相邻项目的差别

- 对照 [[chrome-devtools-mcp]]：后者暴露完整的 DevTools 能力，偏调试和性能分析；agent-browser 偏办事和自动化。
- 同一团队还有操作整个桌面的 agent-desktop（Apache-2.0，约 2.7 万星），属于 computer use 一侧，见 [[Agent电脑与沙箱层]]。

入口：[[indexes/开源项目]]。
