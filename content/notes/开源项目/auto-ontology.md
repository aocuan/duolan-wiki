---
title: auto-ontology
type: 项目卡
tags:
  - 开源项目
  - 本体
  - 语义层
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 研究 · 企业本体
sources:
  - https://github.com/NVIDIA/auto-ontology
publish: true
repo: https://github.com/NVIDIA/auto-ontology
license: Apache-2.0
stars: 15166
verdict: 从元数据自动生成语义层，让 agent 查数据时口径一致、能解释出处；解决读侧 grounding，不解决受控写回
---

# auto-ontology

[NVIDIA Auto Ontology](https://github.com/NVIDIA/auto-ontology) 是一个 Python 框架，从已有数据系统的元数据里自动生成本体：业务概念、指标、实体、关系和血缘，并在多个系统之间对齐定义，再通过 MCP、命令行和 API 交给任意 agent 使用。它的主要用途是让自然语言转 SQL 时有确定的口径，例如「收入」到底对应哪一列、怎么算。许可证 Apache-2.0，星标 15,166，截至 2026-11-26（太平洋时间）。2026 年 11 月初开源后连续几天上了日榜。

## 判断

它解决的是读侧问题：让 agent 读到的数字准确、能说出来源。它不提供对业务对象的受控动作、权限和审计写回，这一块正是 [[操作本体]] 要补的。可以把它当作「语义层 / 知识层」的当代样本。

对照见 [[本体与语义层工具对照]]。入口：[[indexes/开源项目]]。
