---
title: nod
type: 项目卡
tags:
  - 开源项目
  - 个人助手
  - Agent电脑
date: 2026-11-26
updated: 2026-11-27
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/n8n-io/nod
publish: true
repo: https://github.com/n8n-io/nod
license: Apache-2.0
stars: 4407
verdict: n8n 出的「自带电脑的个人 agent」，在真实网站上办事、动手前先问人；体量还小，可对照 OpenMausBot 跟踪
---

# nod

[nod](https://github.com/n8n-io/nod) 是工作流平台 n8n 团队开源的个人 agent。它自带一台电脑，在真实网站上替你办事，例如追发票、准备通话资料、取消试用订阅；执行动作前会先征求同意。运行在你自己的机器上，模型可以自己选。许可证 Apache-2.0，星标 4,407，截至 2026-11-27（太平洋时间）。仓库 2026 年 9 月下旬创建，11 月中旬第一次进周榜，月底仍在周榜上。

## 怎么搭的

- 形态：桌面应用（macOS 为主，Windows 和 Linux 为预览），也可以跑在自己的服务器上；除了应用本身，也能从 Telegram、WhatsApp 和它说话。
- 组成：TypeScript / Node.js，agent 运行时用 [[Pi]]，浏览器操作用 [[agent-browser]]，接外部应用走 MCP 和 Composio，桌面壳是 Electron。
- 模型：自带模型服务商的 key（OpenAI、Anthropic、Gemini 等），也可以用 ChatGPT 订阅登录；用 API 时会显示每个任务的花费，并在月度上限处停下。
- 数据：文件、记忆和保存的登录留在运行它的机器上；但应用连接默认经过 n8n 托管的连接服务，基础使用数据也默认上报，可以在设置里关掉。
- 安全：README 说明安全检查本身是模型判断，项目仍是研究预览，所以凡是用户没要求的动作都先问，并留下记录。

## 判断

它把「个人助手 + 给助手配一台电脑」打包成一个产品，是老牌自动化厂商第一次把它做成独立产品，而不是工作流里的一个节点，方向和 [[OpenMausBot]]、[[Memoh]] 接近。背后是成熟的自动化公司，值得跟踪；但目前体量小，能力边界和安全默认值还要等更多真实使用反馈。自托管时留意两项默认开启的外连：连接服务和使用数据上报。

品类见 [[Personal-Agent品类对照]]、[[Agent电脑与沙箱层]]。入口：[[indexes/开源项目]]。
