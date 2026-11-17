---
title: WikiSkill
type: 论文笔记
tags:
  - 论文
  - Skills
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · Skills 论文
sources:
  - https://arxiv.org/abs/2608.27454
publish: true
---

# WikiSkill

[WikiSkill](https://arxiv.org/abs/2608.27454)（arXiv:2608.27454）是 Google Research 的一篇 skill 进化论文。它要解决的不是再写一份 `SKILL.md`，而是：agent 跑出来的经验如何积累成一份会生长的 wiki，再拿这份知识去改 skill。

作者包括 Liyan Tang、Cyrus Rashtchian、Chun-Sung Ferng、Andrew Tomkins、Da-Cheng Juan、Tu Vu。通讯邮箱写在论文页面上。

## 论文在做什么

已有一些工作会从执行过程里改 skill，但「学到了什么」往往没有单独、可跨轮次累积的表示。WikiSkill 在原始轨迹和可执行 skill 中间加了一层 wiki。

工作区大致分成三层：

- `raw/`：不可变的执行轨迹
- `wiki/`：模式页面，以及提案、验收和回滚记录
- `skills/`：可执行的 `SKILL.md`，并映射回 wiki 里的模式

每轮先用当前 skill 去执行，再由维护者或提案者根据新轨迹更新 wiki 和 skill。被拒绝的提案也要留下记录，避免重复提出。

## 主张与边界

论文想证明的是：把经验编成可检索、可追溯的知识层，比只在轨迹或失败反馈里打转更有复利。对「更大模型更吃 skill」这类说法，文中有限定范围，不能直接外推成定律。

它没有把官方实现作为一个可直接安装的产品仓库发布。公开页面和检索里，看不到作者给出的官方代码库。社区里存在名称相近的其他项目，对应的是不同工作，不能当成这篇论文的官方实现。

## 可借鉴的点

就算不上完整系统，这几条也可以用在手工维护的 [[Skills]] 里：

1. 执行层看不到的模式，单独放进一份可链接的笔记，而不是只改 skill 正文。
2. 被拒绝的改法要记下来，防止下次再提一遍。
3. skill 可以回滚，已经学到的知识不必一起回滚。
4. 小模型在特定环境里写出的权宜之计，不要直接当成可迁移的通用 skill。

和日常用法的关系见 [[Skills]]、[[薄技能与重框架]]。入口：[[indexes/论文]]。
