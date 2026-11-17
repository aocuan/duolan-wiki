---
title: Mem0
type: 项目卡
tags:
  - 开源项目
  - 记忆
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业知识库
sources:
  - https://github.com/mem0ai/mem0
  - https://mem0.ai
publish: true
repo: https://github.com/mem0ai/mem0
license: Apache-2.0
stars: 69095
verdict: 给 agent 加一层可持久记忆的常用薄方案；先用原始记录检索做基线，再决定要不要上它
---

# Mem0

[Mem0](https://github.com/mem0ai/mem0) 给 agent 和应用程序提供可持久的记忆层。官网是 [mem0.ai](https://mem0.ai)。许可证是 Apache-2.0。星标 69,095，统计截至 2026-11-17（太平洋时间）。

## 开源范围

它比 [[Graphiti]] 更薄，更常被用在「记住偏好和关键事实」而不是企业级时效图。上线之前，应先跑「原始记录 + 检索 + 重排」这条基线，见 [[RAW-RAG]] 和 [[RAG与检索手段]]。记忆层和文档问答不是同一件事。

入口：[[indexes/开源项目]]。
