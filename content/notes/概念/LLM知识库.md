---
title: LLM 知识库
type: 概念卡
tags:
  - 概念
  - 企业知识
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业知识库
sources:
  - https://x.com/karpathy/status/2039805659525644595
  - https://llmstxt.org/
  - https://agents.md/
publish: true
---

# LLM 知识库

这里说的不是再买一套向量数据库，而是：把原始材料整理成人和模型都能读的、带链接的笔记，再让模型按文件、标题和双链去检索。公开讨论里，[Karpathy 关于 LLM 知识库的长帖](https://x.com/karpathy/status/2039805659525644595) 是这条思路被广泛引用的起点之一。

## 定义

常见做法很薄：

- 笔记用普通 Markdown，用双链连起来，必要时做成网站。
- 在仓库根目录放给模型看的说明，例如 [[AGENTS-md|AGENTS.md]] 和 [llms.txt](https://llmstxt.org/)，写清目录约定和公开范围。
- 先用全文搜索和链接跳转，不预设必须有一套重型检索服务。

[[WikiSkill]] 从论文一侧呼应了同一想法：经验先写成会累积的 wiki，再回写可执行的 skill。[[Basic-Memory]] 则把普通笔记直接当成跨会话记忆。

## 和相近概念的差别

- 和「切块后做向量检索」：知识库首先是写清楚、连起来，检索是后来加上的能力。见 [[RAG与检索手段]]。
- 和 [[操作本体]]：笔记知识库解决的是读和引用；操作本体还要解决受控写回。
- 和企业知识平台：[[WeKnora]]、[[Onyx]] 这类产品可以服务多人、接权限；个人知识库不必一上来就上平台。落地工具见 [[个人知识库怎么搭]]。

入口：[[indexes/概念]]、[[indexes/企业知识与本体]]。
