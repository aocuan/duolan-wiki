---
title: Harness Engineering
type: 论文笔记
tags:
  - 论文
  - Agent工程
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · Agentic 工程实践
sources:
  - https://arxiv.org/abs/2609.00006
publish: true
---

# Harness Engineering

[Harness Engineering: Anatomy, Architecture, and Evolution of Coding Agents](https://arxiv.org/abs/2609.00006) 剖析了多个编码 agent 的源码构成。对检索实践最常被引用的一条是：这些工具搜索代码时，普遍以路径匹配、文本搜索和语法树为主，而不是先上向量库。

这和 [[Harness]]、[[RAG与检索手段]] 里「代码检索以 grep 打底、结构补位」是同一判断。论文还观察到，技能文件在这些工具里已经相当常见。它研究的是工程构成，不是某一家产品的评测榜。

入口：[[indexes/论文]]。
