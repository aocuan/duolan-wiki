---
title: RAG 与检索手段趋势
type: 主题综述
tags:
  - RAG
  - 检索
  - 综述
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · RAG 检索趋势
sources:
  - https://arxiv.org/abs/2610.35868
  - https://arxiv.org/abs/2610.30755
  - https://arxiv.org/abs/2610.34073
  - https://arxiv.org/abs/2609.00006
  - https://huggingface.co/blog/multi-vector-encoder
publish: true
---

# RAG 与检索手段趋势

观察窗口大约是 2026 年 8 月到 11 月上旬，主要来自公开论文、博客和 X 上的高互动讨论。这不是全量统计，而是对当时讨论中心的归纳。

## 结论

RAG 没有消失，但「切块 → 向量 → top-k」已经不是讨论中心。更值得盯的是五件事：决策模型进入检索链路；朴素检索作为 agent 记忆的强基线重新被强调；检索变成 agent 自己调用的工具；代码场景以 grep 打底、再用结构补位；多向量和重排序走向主流。

「RAG 已死」和「长上下文可以完全取代检索」这两句，热度都在下降。更常见的分法是：长上下文当工作记忆，检索当控制面。通用 GraphRAG 叙事也在变冷，代码图谱这类有结构的用法除外。

## 趋势一：决策模型进入检索链路

决策模型（decision model）这里取窄义：基于 transformer，但不生成长文本，只回答选择、打分、是或否，并给出校准过的概率，延迟往往在百毫秒级。2026 年 9 月 TypeSafe AI 发布 Jev 之后，这个品类开始被单独讨论。

它在检索里的用法包括：路由、重排、过滤，甚至沿着目录从主题走到段落。较激进的做法是 [DecisionRAG](https://arxiv.org/abs/2610.35868)（Retriever-Free Retrieval）：不做传统的第一阶段检索器，让决策模型在文档结构里导航。论文报告在 Natural Questions 上 Hit@1 高于「稠密检索 + 8B 重排」的设定，单次大约 0.7 到 1.8 秒。这些数字来自论文，第三方复现仍少；Jev 本身是托管接口。更稳妥的试验顺序是先把它放在「重排和过滤」这一步，而不是整条链路替换。

## 趋势二：朴素检索作为记忆基线

过去一年出现过不少把对话改写成事实条目的 agent 记忆层。2026 年 10 月的 [RAW-RAG](https://arxiv.org/abs/2610.30755) 和 [Memory Tax](https://arxiv.org/abs/2610.34073) 给出一个反向结果：直接对原始记录做检索再重排，多数设置里不弱于更复杂的记忆系统，建造索引也更便宜。一个常见解释是，改写会丢掉或扭曲事实之间的关联。

实用含义很直接：给 agent 加记忆层之前，先跑「原始材料 + 检索 + 重排」这条基线。agent 记忆本质上仍是检索问题。这也和 [[企业知识库开源选型]] 里「先分清问答层和记忆层」是同一件事。

## 趋势三：检索变成 agent 的工具

固定 top-k 流水线在讨论里确实在退场，换成 agent 自己决定搜什么、搜几次、要不要换关键词。竞争转到三处：给 agent 用的搜索接口和排行（例如 Artificial Analysis 的 Search Index）、用强化学习训练的搜索 agent，以及不用向量、靠目录树加推理走动的「无向量」检索（PageIndex 一类）。后者更适合结构清楚的长文档，例如年报、合同、手册，也是 DecisionRAG 的前身思路。

一个工程上的提醒：模型推理越来越便宜时，搜索费用可能反而成为 agent 任务里显眼的一项。

## 趋势四：代码检索是 grep 打底、结构补位

[Harness Engineering](https://arxiv.org/abs/2609.00006) 对多个编码 agent 的源码做了剖析，观察到代码搜索普遍以 ripgrep、glob、tree-sitter 和 Markdown 上下文文件为主，而不是先上向量库。社区补的方向主要是：把代码库做成可查询的结构图，或在 grep 之外加一层语义判断。

结论可以记成：grep 是地板，不是天花板。代码已经自带路径、符号和引用关系，「结构 + grep」通常比「纯向量」更受欢迎；语义检索更适合「知道行为、不知道在哪」的情况。这和 [[Harness]]、[[AGENTS-md|AGENTS.md]] 的工程实践是一致的。

## 趋势五：多向量与重排序

单向量装不下一段文本的全部细节，这个限制被反复提起。ColBERT 式的后期交互（每个词一个向量，查询时再交互）因此回到主流视野。[Sentence Transformers 关于多向量模型的说明](https://huggingface.co/blog/multi-vector-encoder) 把它降到了更容易用的位置，后续工作则在压缩存储和计算。另一侧，重排序器和视觉文档检索（直接对页面图像检索、减少对 OCR 的依赖）也在更新。

生产里常见的组合仍是：稠密加词法混合召回，再用多向量或重排序做精排。

## 值得读的公开材料

- [DecisionRAG](https://arxiv.org/abs/2610.35868)
- [RAW-RAG](https://arxiv.org/abs/2610.30755)
- [Memory Tax](https://arxiv.org/abs/2610.34073)
- [Harness Engineering](https://arxiv.org/abs/2609.00006)
- [FLINT](https://arxiv.org/abs/2610.27273)
- [Multi-Vector Embedding Models with Sentence Transformers](https://huggingface.co/blog/multi-vector-encoder)
- [How Jev can help improve the efficiency of RAG pipelines](https://www.thoughtworks.com/en-us/insights/blog/generative-ai/how-jev-can-help-improve-the-efficiency-of-rag-pipelines)（Thoughtworks）
- [jev-reranker](https://huggingface.co/blog/hotchpotch/introducing-jev-reranker)

后续的按期补充，适合写进 `notes/趋势/`，不要覆盖这篇的主判断，除非大方向已经变了。相关入口：[[indexes/RAG检索]]。
