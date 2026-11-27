---
title: Beacon
type: 项目卡
tags:
  - 开源项目
  - 会话归档
  - 记忆
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/Asymptote-Labs/agent-beacon
publish: true
repo: https://github.com/Asymptote-Labs/agent-beacon
license: MIT
stars: 3607
verdict: 跨 harness 记录完整会话并沉淀成可复用经验；适合想让经验跨工具累积的人，装时留意存储位置
---

# Beacon

[Beacon](https://github.com/Asymptote-Labs/agent-beacon)（仓库名 agent-beacon）给编码 agent 做跨工具的记忆层：采集 Claude Code、Cursor、Codex、OpenCode 等 20 多种 harness 的完整会话，包括提示、回复、工具调用、命令、改动和审批，再把其中有用的工作流、纠错和调试套路整理成后续 agent 可以通过 MCP 或 Skills 取用的知识。许可证 MIT，星标 3,607，截至 2026-11-26（太平洋时间）。

## 开源范围

本地运行的部分在仓库里，记录以 JSONL 形式落盘；同时有官方云版本。调研时社区反馈是推广味较重，安装流程里云端选项比较显眼，想纯本地使用要主动确认存储位置。

## 和相邻项目的差别

- 对照 [[AgentsView]]：AgentsView 是档案馆，Beacon 想把档案变成下一次能用的经验。
- 对照 [[deja-vu]]：两者目标接近，deja-vu 更轻，不调用模型。
- 对照 [[claude-mem]]：claude-mem 主要服务单一编码工具的跨会话上下文；Beacon 强调跨 harness。

选型见 [[Agent会话归档工具对照]]。入口：[[indexes/开源项目]]。
