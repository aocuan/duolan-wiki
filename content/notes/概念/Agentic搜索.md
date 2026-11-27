---
title: Agentic 搜索
type: 概念卡
tags:
  - 概念
  - RAG
  - 检索
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 监控 · RAG 检索趋势
sources:
  - https://arxiv.org/abs/2610.41172
  - https://arxiv.org/abs/2605.10848
  - https://arxiv.org/abs/2605.05242
  - https://arxiv.org/abs/2605.15184
  - https://arxiv.org/abs/2609.00006
publish: true
---

# Agentic 搜索

## 定义

Agentic 搜索指的是：不再「一次向量检索取 top-k 就交给模型」，而是让模型在循环里自己写查询、调用 BM25 或 grep 这类词法工具、看结果、改查询、判断够不够，再决定是否继续。语义理解交给模型反复改写查询来完成；检索工具只需要准、便宜、不用维护索引。

## 为什么现在常被提起

- 多篇独立研究得到相近结论：在强模型驱动的循环里，词法检索已经够用。例如 [Pi-Serini](https://arxiv.org/abs/2605.10848) 用调好的 BM25 在 BrowseComp-Plus 上取得高分；[Direct Corpus Interaction](https://arxiv.org/abs/2605.05242) 只用 grep、读文件和 shell 就超过了稀疏、稠密和重排基线；[Is Grep All You Need?](https://arxiv.org/abs/2605.15184) 讨论了 harness 如何改变检索；[[Context-as-Infrastructure]] 发现加稠密向量腿反而让准确率下降。
- 编码 agent 普遍以 grep 为默认代码检索方式，见 [[Harness-Engineering]]。代码索引会过期，grep 读的永远是最新文件。
- 竞争维度变了：在这类基准上准确率接近饱和以后，比的是 token、延迟和可追溯性，而不只是 Recall@k。

## 边界

- 现有证据大多来自英文维基类基准、前沿模型和很高的 token 预算。换成表格多、扫描件多、行话多的语料，结论可能反转。
- 大型代码库里，语义搜索仍能补位；更常见的结论是混合检索最好，grep 是地板不是天花板。
- 「BM25 + grep 就够」的基准，可能奖励的是查找而不是推理。

## 和相近概念的差别

- 和 [[决策模型检索]]：Agentic 搜索把判断交给生成式模型的循环；决策模型检索用不生成文字的模型一次给一批候选打分，更快更省。两者常一起用。
- 和 [[PageIndex]] 这类目录导航：都不依赖向量库，但目录导航需要事先把文档整理成层级结构。

综述见 [[RAG与检索手段]]。入口：[[indexes/概念]]、[[indexes/RAG检索]]。
