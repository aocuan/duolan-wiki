---
title: Search When Needed：按中间结论可靠度奖励的搜索 RL
type: 论文笔记
tags:
  - 论文
  - RAG
  - 强化学习
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 监控 · RAG 检索趋势
sources:
  - https://arxiv.org/abs/2610.41738
  - https://arxiv.org/abs/2503.09516
publish: true
---

# Search When Needed：按中间结论可靠度奖励的搜索 RL

原题 *Search When Needed, Proceed When Reliable: Metacognitive Reliability Supervision for Efficient Agentic Search*（[arXiv:2610.41738](https://arxiv.org/abs/2610.41738)，2026-10-30）。

## 论文在做什么

[Search-R1](https://arxiv.org/abs/2503.09516) 这类方法用强化学习教模型边推理边搜索，但只按最终答案对错给奖励。这样分不清蒙对的、多搜几轮才对的、搜到了有用证据但后面推理错的，于是模型可能该搜时不搜、不该搜时乱搜。

这篇论文给中间步骤加了一种「可靠度」信号：用模型写出的中间结论的 token 平均负对数似然估计不确定度，再映射成「这一步结论靠谱的概率」。结论靠谱就继续推理，不靠谱才去搜索，奖励也按这个过程来给。

## 主张与边界

- 作者报告：比最强基线高约 2.1 分，搜索次数少约 6.8%；多跳问题上反而会多搜几次，符合「该搜才搜」。训练每步慢约 14.6%。
- 实验环境受控：所有方法共用同一个 E5-base 稠密检索器和维基索引，每次取 3 段，最多搜 4 轮。
- 提升方向对，但幅度不大；代码和权重在论文发布时写的是「将开源」。

## 可借鉴的点

检索要不要发生、发生几次，正在从固定流程变成模型策略的一部分。这条线和 [[决策模型检索]]、[[Agentic搜索]] 是同一个趋势：把「搜什么、够不够」的判断交给模型。

入口：[[indexes/论文]]、[[indexes/RAG检索]]。
