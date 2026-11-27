---
title: Letta
type: 项目卡
tags:
  - 开源项目
  - 记忆
  - Agent平台
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/letta-ai/letta
publish: true
repo: https://github.com/letta-ai/letta
license: Apache-2.0
stars: 25563
verdict: 有状态 agent 平台的老牌代表（前身 MemGPT）；思路有影响力，但主仓近期更新放缓
---

# Letta

[Letta](https://github.com/letta-ai/letta) 是做「有状态 agent」的平台，前身是提出分层记忆思路的 MemGPT。agent 的记忆、工具和状态由服务端统一管理，可以长期运行并自我修改记忆。许可证 Apache-2.0，星标 25,563，截至 2026-11-26（太平洋时间）。主仓最近一次推送是 2026-10-18，比同类项目慢。

## 判断

它对「agent 自己管理上下文窗口」这一类设计影响很大，概念上值得了解。但如果只是想给现有 agent 加一层记忆，更轻的 [[Mem0]]、[[Hindsight]] 更容易接；Letta 更像一整套 agent 运行平台。

地图见 [[Agent知识库项目地图]]。入口：[[indexes/开源项目]]。
