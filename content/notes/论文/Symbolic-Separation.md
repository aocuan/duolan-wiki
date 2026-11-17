---
title: Symbolic Separation
type: 论文笔记
tags:
  - 论文
  - 企业知识
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业本体
sources:
  - https://arxiv.org/abs/2609.17107
publish: true
---

# Symbolic Separation

[Symbolic Separation: Grounding Deep Agents in Knowledge Graphs for Trustworthy Operational Data Analytics](https://arxiv.org/abs/2609.17107) 主张：模型可以自由推理，但碰到真实数据、尤其是要执行动作时，只能走被本体约束过的虚拟知识图，并在执行前做确定性校验。

这和「先检索一段文字再生成」不是同一件事，更接近 [[操作本体]] 里「读路径不能靠模型猜关系、写路径要过闸」的判断。论文本身偏分析和校验，并不是完整的写回平台。文中报告的实验数字来自作者，第三方复现仍少，当作旁证即可。

相邻：[[EvoOntology]]、[[ContrAgent]]。入口：[[indexes/论文]]。
