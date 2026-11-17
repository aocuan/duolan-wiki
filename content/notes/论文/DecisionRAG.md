---
title: DecisionRAG
type: 论文笔记
tags:
  - 论文
  - RAG
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · RAG 检索趋势
sources:
  - https://arxiv.org/abs/2610.35868
publish: true
---

# DecisionRAG

[Retriever-Free Retrieval: Navigating Documents with Decision Models](https://arxiv.org/abs/2610.35868) 提出 DecisionRAG：不用传统的第一阶段检索器，让 [[决策模型检索|决策模型]] 在文档结构里导航。

论文报告在 Natural Questions 等设定上，命中率高于「稠密检索加大型重排」的组合，单次大约 0.7 到 1.8 秒。这些数字来自论文，第三方复现仍少。更稳妥的用法是先把决策模型放在重排和过滤，而不是整条链路替换。

背景和相邻工作见 [[RAG与检索手段]]。入口：[[indexes/论文]]。
