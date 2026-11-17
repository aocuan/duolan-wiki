---
title: Agent 记忆与聊天记录工具
type: 主题综述
tags:
  - 企业知识
  - 记忆
  - 综述
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业知识库
sources:
  - https://arxiv.org/abs/2610.30755
  - https://github.com/mem0ai/mem0
  - https://github.com/getzep/graphiti
  - https://github.com/nowledge-co/nowledge-mem
  - https://github.com/basicmachines-co/basic-memory
publish: true
---

# Agent 记忆与聊天记录工具

「让 agent 记住」和「在一堆聊天记录里找回那一次对话」常被当成同一件事。其实至少有三层，选型时不要混用。

## 先分三层

1. **原始记录检索**：把对话或材料原样存下来，做检索和重排。[[RAW-RAG]] 和 [[Memory-Tax]] 的结果是，这条基线在不少设置里不弱于更复杂的记忆系统。见 [[RAG与检索手段]]。
2. **记忆层**：把对话改写成事实、偏好或带有效期的图谱，再在下一步喂给模型。[[Mem0]] 更薄，偏偏好和关键事实；[[Graphiti]] 更重，偏会随时间变化的实体和关系。托管版会再包一层权限和审计，和开源内核不是同一个交付物。
3. **跨工具的个人上下文管理**：把多个 AI 工具里的线程收拢，便于查找。[[Nowledge-Mem]] 走这条产品路线，但主仓没有标准开源许可证，不能按完全开源来用。[[Basic-Memory]] 则把普通 Markdown 笔记当成跨会话记忆，许可证是 AGPL-3.0。

## 怎么选

- 任何记忆产品上线前，先跑原始记录检索这条基线。
- 文档、手册、Wiki 用知识库或解析层，例如 [[RAGFlow]]、[[WeKnora]]、[[Onyx]]，不要塞进记忆图谱。
- 只想记住个人或项目习惯，先看笔记式方案和 [[LLM知识库]]，不必一上来上图数据库。
- 「必须完全开源才能用」时，先核对许可证：没有标准许可证的产品，只适合按专有工具评估。

入口：[[indexes/企业知识与本体]]。
