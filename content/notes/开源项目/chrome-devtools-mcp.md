---
title: chrome-devtools-mcp
type: 项目卡
tags:
  - 开源项目
  - 浏览器
  - MCP
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/ChromeDevTools/chrome-devtools-mcp
publish: true
repo: https://github.com/ChromeDevTools/chrome-devtools-mcp
license: Apache-2.0
stars: 59542
verdict: Chrome 官方给编码 agent 的 DevTools 接口；前端调试、性能分析时首选
---

# chrome-devtools-mcp

[chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp) 是 Chrome DevTools 团队发布的 agent 接口，以 MCP 服务和命令行两种形式提供。编码 agent 可以控制并检查一个真实运行的 Chrome：看网络请求和控制台、录性能追踪、做可靠的自动化。许可证 Apache-2.0，星标 59,542，截至 2026-11-26（太平洋时间）。

## 判断

前端开发里，「写完代码让 agent 自己打开页面查问题」这一步，官方接口比第三方方案稳。它偏调试和性能分析；只想让 agent 在网页上办事，用 [[agent-browser]] 这类命令行工具更省上下文。

入口：[[indexes/开源项目]]。
