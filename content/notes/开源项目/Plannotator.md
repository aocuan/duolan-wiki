---
title: Plannotator
type: 项目卡
tags:
  - 开源项目
  - 人机协作
  - 评审
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/backnotprop/plannotator
publish: true
repo: https://github.com/backnotprop/plannotator
license: Apache-2.0
stars: 15308
verdict: 在浏览器里给 agent 的计划、文档和代码改动做批注，再把意见回传给 agent；人机协作审阅的轻量层
---

# Plannotator

[Plannotator](https://github.com/backnotprop/plannotator) 是给编码 agent 用的本地审阅界面。agent 提出计划、写完文档或改完代码时，浏览器里打开对应内容，人可以批注、评论 diff、提修改建议，意见再直接发回 agent 执行。它通过插件、hooks 和命令接入 Claude Code、Codex、Gemini CLI、OpenCode、Pi 等工具。许可证 Apache-2.0，星标 15,308，截至 2026-11-26（太平洋时间）。

## 判断

多 agent 并行干活以后，人的瓶颈从「写」变成「看和拍板」。Plannotator 补的就是这一层：把审阅变成结构化反馈，而不是在聊天框里来回打字。它可以和 [[Herdr]] 等调度工具搭配。

## 和相邻项目的差别

- 对照 [[HumanLayer]]：HumanLayer 偏审批和人在回路的流程；Plannotator 偏对计划和改动做批注。
- 和 [[AI-Native组织对照]] 里的团队房间不同，它不是沟通渠道，而是审阅界面。

入口：[[indexes/开源项目]]。
