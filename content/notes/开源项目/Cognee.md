---
title: Cognee
type: 项目卡
tags:
  - 开源项目
  - 记忆
  - 知识图谱
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/topoteretes/cognee
  - https://docs.cognee.ai
publish: true
repo: https://github.com/topoteretes/cognee
license: Apache-2.0
stars: 33662
verdict: 自动抽取并合并事实、搭知识关系的记忆平台；适合需要结构化记忆的场景，效果数字多为厂商自测
---

# Cognee

[Cognee](https://github.com/topoteretes/cognee) 是开源的 agent 记忆平台：从文档、对话和外部来源里自动抽取实体与关系，合并重复事实，形成可检索的知识结构，也支持自定义数据模型和本体。许可证 Apache-2.0，星标 33,662，截至 2026-11-26（太平洋时间）。

## 开源范围

核心库完整开源，可以自托管；另有商业云。2026 年 11 月官方介绍了一套只用开放权重模型加 Postgres、不依赖图数据库的方案，用来从代码仓库、聊天工具和文档工具里自动搭出组织知识关系。官方报的 LoCoMo、BEAM 分数属于厂商自测。

## 判断

扫榜里多次出现，但本知识库还没有对它做过实测。它介于「记忆层」和「知识图谱」之间：比 [[Mem0]] 重，比自己搭 [[Graphiti]] 省事。

## 和相邻项目的差别

- 对照 [[Graphiti]]：Graphiti 强调时间有效期；Cognee 强调自动抽取和合并。
- 对照 [[LightRAG]]：LightRAG 是图检索的 RAG 框架，Cognee 更像记忆平台。
- 本体方向的工具见 [[本体与语义层工具对照]]。

地图见 [[Agent知识库项目地图]]。入口：[[indexes/开源项目]]。
