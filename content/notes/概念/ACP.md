---
title: ACP
aliases:
  - Agent Client Protocol
type: 概念卡
tags:
  - 概念
  - Agent工程
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://agentclientprotocol.com
  - https://github.com/agentclientprotocol/agent-client-protocol
publish: true
---

# ACP

ACP（Agent Client Protocol）是一套用来连接编辑器或控制面和编码 agent 的开放协议。官方说明见 [agentclientprotocol.com](https://agentclientprotocol.com)，规范仓库是 [agentclientprotocol/agent-client-protocol](https://github.com/agentclientprotocol/agent-client-protocol)（Apache-2.0，约 4,663 星，截至 2026-11-17，太平洋时间）。

## 定义

有了 ACP，控制面不必为每一种编码工具各写一套私有接线。[[Lody]]、[[Paseo]] 以及 [[Buzz]] 对部分编码 agent 的接入，都走这一层：调度的是「已经在跑的 agent 会话」，而不是把模型重新包一遍。

它不是产品，而是接口约定。一个自称支持 ACP 的仓库，仍要单独看它开了哪些客户端、同步是否依赖官方云。

## 和相近概念的差别

- 和 [[Harness]]：harness 是某一个 agent 的工位；ACP 是控制面和多个 harness 之间的插头。
- 和 [[Skills]]：Skills 是按需加载的说明书；ACP 不管说明书长什么样。

相关项目见 [[Personal-Agent品类对照]]。入口：[[indexes/概念]]。
