---
title: EvoOntology
type: 论文笔记
tags:
  - 论文
  - 企业知识
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业本体
sources:
  - https://arxiv.org/abs/2609.15779
publish: true
---

# EvoOntology

[EvoOntology: A Self-Evolving Ontology Layer for Data Agents](https://arxiv.org/abs/2609.15779) 把给数据 agent 用的本体拆成三层：类型和引用规则、领域知识与数据映射，以及可调用的工具接口，并讨论这三层如何一起演化。

它和设计期先写类型、再生成存储结构的做法是一条路上的不同阶段：前者强调运行时也可以改结构，后者强调先把类型源定住。对照时不要把「能演化」理解成可以跳过闸门。背景见 [[操作本体]]。

相邻：[[Symbolic-Separation]]。入口：[[indexes/论文]]。
