---
title: Graphiti
type: 项目卡
tags:
  - 开源项目
  - 记忆
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业知识库
sources:
  - https://github.com/getzep/graphiti
  - https://help.getzep.com/graphiti
publish: true
repo: https://github.com/getzep/graphiti
license: Apache-2.0
stars: 32874
verdict: 会随时间变化的事实记忆层里，开源内核最像样的一档之一；不要拿它当文档库
---

# Graphiti

[Graphiti](https://github.com/getzep/graphiti) 用来给 AI agent 建实时知识图谱。文档见 [help.getzep.com/graphiti](https://help.getzep.com/graphiti)。许可证是 Apache-2.0。星标 32,874，统计截至 2026-11-17（太平洋时间）。

## 开源范围

它是开源内核：自己接图数据库，自己管用户和会话。托管产品是另一层，会把权限、审计和运行环境包进去。用法大致是：把一段对话或业务事件送进去，由模型抽出实体、关系和有效期；旧事实不是直接删掉，而是标成失效。

它擅长「会变的事实」，不擅长当 PDF 或 Wiki 文档库。每条事件都要调用模型，小模型若抽不稳就会失败；没有类型约束地乱喂，也容易变成一堆同名实体。文档库请看 [[RAGFlow]] 或 [[WeKnora]]，对照见 [[Agent记忆与聊天记录工具]]。

入口：[[indexes/开源项目]]。
