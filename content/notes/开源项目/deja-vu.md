---
title: deja-vu
type: 项目卡
tags:
  - 开源项目
  - 会话归档
  - 记忆
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/vshulcz/deja-vu
publish: true
repo: https://github.com/vshulcz/deja-vu
license: MIT
stars: 1681
verdict: 轻量的个人方案：直接读本机已有的会话日志做记忆和召回，不调用模型；基本是个人维护
---

# deja-vu

[deja-vu](https://github.com/vshulcz/deja-vu) 给编码 agent 提供本地记忆：直接读取磁盘上已有的会话日志，为五十多种 agent 建索引，支持跨会话搜索、在不同 agent 之间交接，也能找回被覆盖的代码。它是单个 Go 二进制，不调用大模型，也不需要 API key。许可证 MIT，星标 1,681，截至 2026-11-26（太平洋时间）。

## 开源范围

完整开源，可以本地运行，通过 MCP 接进 Claude Code、Codex、Cursor 等工具。多台机器之间靠导入导出或 SSH 同步。

## 判断

适合想要免费、轻量的自动召回，又不想多跑一个服务的人。主要风险是维护者集中。

## 和相邻项目的差别

- 对照 [[Beacon]]：Beacon 更完整、有云版；deja-vu 更轻、全本地。
- 对照 [[AgentsView]]：AgentsView 偏浏览和统计，deja-vu 偏召回和交接。

选型见 [[Agent会话归档工具对照]]。入口：[[indexes/开源项目]]。
