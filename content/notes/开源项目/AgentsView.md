---
title: AgentsView
type: 项目卡
tags:
  - 开源项目
  - 会话归档
  - 记忆
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/kenn-io/agentsview
  - https://agentsview.io/docs/
publish: true
repo: https://github.com/kenn-io/agentsview
license: MIT
stars: 6550
verdict: 只想把各家编码 agent 的会话集中归档、能搜、能看花费时的首选；不负责「自动记住经验」
---

# AgentsView

[AgentsView](https://github.com/kenn-io/agentsview) 是编码 agent 的本地会话档案馆：读取 Claude Code、Codex 等 50 多种 agent 已经写在磁盘上的会话记录，统一浏览、全文搜索，并统计 token 用量和花费。许可证 MIT，星标 6,550，截至 2026-11-26（太平洋时间）。

## 开源范围

整套都在仓库里，可以完全自托管，数据默认留在本机。多台机器的记录可以通过 SSH 或共享数据库归到一处。语义搜索是可选项，不开就不额外消耗模型费用。

使用时注意两点：默认会发送匿名使用统计，按文档可以关掉；统计面板的数字适合看趋势，不宜当精确账本。

## 和相邻项目的差别

- 对照 [[Beacon]]、[[deja-vu]]：那两个更偏「让下一次 agent 用上以前的经验」；AgentsView 偏「把原始会话存好、找得到」。
- 对照 [[Nowledge-Mem]]：后者核心闭源，会把对话提炼成记忆；AgentsView 不提炼，只归档和检索。
- 对照 [[Lody]]、[[Omnigent]]：那些是多端接手同一个会话，不负责导入历史。

选型见 [[Agent会话归档工具对照]]。入口：[[indexes/开源项目]]。
