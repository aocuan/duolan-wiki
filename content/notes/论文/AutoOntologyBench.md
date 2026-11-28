---
title: AutoOntologyBench
type: 论文笔记
tags:
  - 论文
  - 企业知识
  - 本体
date: 2026-11-27
updated: 2026-11-27
status: evergreen
source_bot: 研究 · 企业本体
sources:
  - https://arxiv.org/abs/2611.27734
  - https://github.com/VinyehShaw/AutoOntologyBench
publish: true
---

# AutoOntologyBench

[AutoOntologyBench: A Task-Grounded Benchmark for Agentic Knowledge Engineering](https://arxiv.org/abs/2611.27734)（arXiv，2026-11-20 提交）问的是：agent 自己搭的本体，能不能帮它把真实任务做得更好，和其他知识表示相比有没有可量化的收益。代码和数据在 [VinyehShaw/AutoOntologyBench](https://github.com/VinyehShaw/AutoOntologyBench)（Apache-2.0）。

## 做了什么

- 19,947 道经过审核的任务，来自 7 个领域的 18 个真实知识源，答案能回到原始知识源核验。
- 任务分四类：应用（Application）、修复（Repair）、组织（Organization）、构建（Construction）。
- 在相同知识表示条件下，比较 9 个前沿模型驱动的 agent。

## 结论

摘要给出的数字：在检索之上叠加 agent 自建的本体，任务成功率提高 6.1 个百分点；但比专家给出的参考本体仍低 13.0 个百分点。作者认为瓶颈在于 agent 自主获取知识。

## 判断

- 它评的是本体「读」的价值，也就是帮 agent 答题和完成任务；没有涉及受控写回，即动作、权限和审计。这一格见 [[操作本体]]。
- 它支持一个常见看法：自动生成本体有提升，但对象和关系的含义由懂行的人来定，效果明显更好。和 [[auto-ontology]]、[[EvoOntology]] 这类「自动建、可演化」的路线对照着看。
- 数字来自学术基准，不能直接推到生产环境。

相邻：[[Symbolic-Separation]]、[[本体与语义层工具对照]]。入口：[[indexes/论文]]。
