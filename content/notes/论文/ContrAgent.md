---
title: ContrAgent
type: 论文笔记
tags:
  - 论文
  - 企业知识
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业本体
sources:
  - https://arxiv.org/abs/2609.18128
publish: true
---

# ContrAgent

[Symbolic Temporal Supervision of LLM Agents Using Contracts](https://arxiv.org/abs/2609.18128) 介绍 ContrAgent：把可检查的时序契约编成自动机，既能在线拦住工具调用，也能离线审计已经发生的轨迹。契约库和具体模型是分开的。

它不太谈对象怎么建模，但和 [[操作本体]] 里「动作的前置条件与审计要写在模型外面」是同一类安全观：规则不靠提示词临时记住。相邻：[[Symbolic-Separation]]。入口：[[indexes/论文]]。
