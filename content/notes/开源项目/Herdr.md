---
title: Herdr
type: 项目卡
tags:
  - 开源项目
  - 会话控制面
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · Personal Agent
sources:
  - https://github.com/herdrdev/herdr
  - https://herdr.dev
publish: true
repo: https://github.com/herdrdev/herdr
license: Apache-2.0
stars: 51496
verdict: 给已有编码 CLI 提供持久运行时和分路调度，本身不是又一个写代码的模型
---

# Herdr

[Herdr](https://github.com/herdrdev/herdr) 称自己是编码 agent 居住的运行时：在本机或远程机器上挂起已经在用的 Claude Code、Codex、OpenCode 等，做分路、派活和跟进。官网是 [herdr.dev](https://herdr.dev)。许可证是 Apache-2.0。星标 51,496，统计截至 2026-11-17（太平洋时间）。

## 开源范围

它调度的是你已经安装的 CLI，而不是再发明一个编码模型。和 [[Lody]]、[[Paseo]] 同属会话控制面 / 多路调度，但更偏终端和持久进程，而不是完整的跨设备云同步产品。

## 和相邻项目的差别

- 对照 [[Lody]]：Lody 强调共享同一个 live session；Herdr 强调 agent 在哪些机器的 pane 里继续跑。
- 对照 [[Pi]]：Herdr 可以接入包括 Pi 在内的工具，自身是运行时而不是循环库。

品类见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
