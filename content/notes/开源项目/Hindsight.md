---
title: Hindsight
type: 项目卡
tags:
  - 开源项目
  - 记忆
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/vectorize-io/hindsight
  - https://hindsight.vectorize.io
  - https://arxiv.org/abs/2512.12818
publish: true
repo: https://github.com/vectorize-io/hindsight
license: MIT
stars: 63755
verdict: 2026 年下半年最热的 agent 记忆层之一，主打「从使用中学习」；选型时先和原始记录检索基线比
---

# Hindsight

[Hindsight](https://github.com/vectorize-io/hindsight) 是 Vectorize 开源的 agent 记忆系统。它的定位不是「记住聊天记录」，而是让 agent 从使用中学习：把经历整理成可以复用的经验和判断。许可证 MIT，星标 63,755，截至 2026-11-26（太平洋时间）。配套有[论文](https://arxiv.org/abs/2512.12818)、基准页面和托管云。

## 开源范围

记忆服务和客户端在仓库里，可以自托管。2026 年 11 月官方又放出了专门给 agent 记忆用的决策、重排和向量模型，权重公开，也可以用官方托管推理。托管云是另一层商业服务。

## 判断

在这一轮 agent 记忆项目里热度最高、增长最快，值得持续跟踪。但它的效果数字主要来自官方基准。和其他记忆层一样，上线前先跑「原始记录 + 检索 + 重排」基线，见 [[RAW-RAG]]、[[Memory-Tax]]。

## 和相邻项目的差别

- 对照 [[Mem0]]：Mem0 更薄，偏偏好和关键事实；Hindsight 强调学习和反思。
- 对照 [[Graphiti]]：Graphiti 是带有效期的关系图；Hindsight 不以图谱为卖点。
- 和「决策模型进检索链路」的趋势一致，见 [[决策模型检索]]。

地图见 [[Agent知识库项目地图]]。入口：[[indexes/开源项目]]。
