---
title: PageIndex
type: 项目卡
tags:
  - 开源项目
  - 检索
  - 无向量
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 监控 · RAG 检索趋势
sources:
  - https://github.com/VectifyAI/PageIndex
  - https://arxiv.org/abs/2610.41172
publish: true
repo: https://github.com/VectifyAI/PageIndex
license: MIT
stars: 40799
verdict: 不用向量库、让模型按目录树定位长文档的代表；适合单份长文档精确定位，不适合当整个资料库的唯一检索
---

# PageIndex

[PageIndex](https://github.com/VectifyAI/PageIndex) 主张「无向量、基于推理的 RAG」：先把长文档整理成类似目录的树，再让模型像人翻书一样沿目录逐层定位，不切块、不建向量库。许可证 MIT，星标 40,799，截至 2026-11-26（太平洋时间）。

## 开源范围

开源仓库提供本地模式的 SDK 和索引方法。公司另有托管云、页面检索和字段抽取等商业 API。

## 判断

- 适合：单份很长、结构清楚的文档（手册、规范、合同类长文）里精确找到条款，并给出可追溯的页码。
- 不适合：当成整个资料库的唯一检索方式。文档一多，仍需要全文或混合检索先缩小范围。
- 热度：2026 年上半年涨得很快，11 月起明显降温，公开讨论里多是旧文改写和推广。一项把多种结构叠加在 BM25 加 grep 循环上的实验发现，PageIndex 式大纲在小规模上持平，在更大规模上反而变差，见 [[Context-as-Infrastructure]]。

## 和相邻项目的差别

- 对照 [[DecisionRAG]]：两者都沿层级结构导航；DecisionRAG 用不生成文字的决策模型打分。
- 对照 [[RAGFlow]]：RAGFlow 是完整的知识库平台；PageIndex 是一种检索方式。

概念见 [[Agentic搜索]]。地图见 [[Agent知识库项目地图]]。入口：[[indexes/开源项目]]。
