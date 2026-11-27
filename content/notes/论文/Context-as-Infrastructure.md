---
title: Context as Infrastructure：给 harness 用的知识编译
type: 论文笔记
tags:
  - 论文
  - RAG
  - 检索
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 监控 · RAG 检索趋势
sources:
  - https://arxiv.org/abs/2610.41172
publish: true
---

# Context as Infrastructure：给 harness 用的知识编译

原题 *Context as Infrastructure: Knowledge Compilation for Retrieval in Agentic Systems with Harnesses*（[arXiv:2610.41172](https://arxiv.org/abs/2610.41172)，2026-10-30），作者来自 RAGFlow 背后的团队。

## 论文在做什么

作者搭了一个只用 BM25 和 grep 的检索 harness，再测试在上面叠加各种「结构化编译」（摘要树、LLM wiki、实体图、类似 PageIndex 的大纲）是否有帮助。流程大致是：

1. 语料没有编译过结构时，连导航工具的描述都不给模型看。
2. 第一次调用模型之前，先在全库做一次扁平的证据召回。
3. 按证据条数、来源多样性和问题覆盖度判断够不够。够就直接回答；不够就整块丢掉，不硬塞进上下文。
4. 不够时才进入 BM25 / grep 工具循环，并行调用，有步数和时间上限。
5. 循环异常结束时，用已有证据拼一个答案，或明确报告失败。

## 主张与边界

- 只用这套 harness，在 BrowseComp-Plus 和 FRAMES 上就达到很高的准确率，但 token 消耗也很大。
- 叠加摘要树、wiki、实体图后准确率没有可辨别的变化；类似 PageIndex 的大纲在小规模持平、大规模变差；加稠密向量检索反而下降。
- 「证据够用就直接答」能大幅省 token；用决策模型做门控能明显降低延迟。
- 作者自己的定位：结构化编译不是更好的检索器，而是「供给层」，作用是让进入上下文的内容更少、可溯源。
- 局限也写明了：只在一个基准、一个抽取模型上测，每个变体只跑一次，没有置信区间；英文维基语料的结论换到表格、扫描件、行话多的语料可能反转。

## 可借鉴的点

- 检索的控制权正在从索引移到循环，见 [[Agentic搜索]]。
- 「先判断证据够不够，再决定要不要搜」是很便宜的优化，和 [[决策模型检索]] 一致。
- 给 agent 的知识库，先保证原文可检索、可追溯，再考虑要不要加图谱或摘要层，见 [[LLM知识库]]。

入口：[[indexes/论文]]、[[indexes/RAG检索]]。
