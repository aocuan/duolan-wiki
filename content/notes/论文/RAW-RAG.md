---
title: RAW-RAG
type: 论文笔记
tags:
  - 论文
  - RAG
  - 记忆
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · RAG 检索趋势
sources:
  - https://arxiv.org/abs/2610.30755
publish: true
---

# RAW-RAG

[Is Complex Agentic Memory Always Needed? Naive RAG Is Stronger Than We Thought](https://arxiv.org/abs/2610.30755) 的核心结果是：直接对原始记录做检索再重排，在多数对照里不弱于把对话改写成记忆条目的系统，建造索引也更便宜。

一个常见解释是，改写会丢掉或扭曲事实之间的关联。实用含义：给 agent 加记忆层之前，先跑这条基线。相邻的价值拆分见 [[Memory-Tax]]，选型见 [[Agent记忆与聊天记录工具]]。

入口：[[indexes/论文]]。
