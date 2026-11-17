---
title: AGENTS.md
aliases:
  - 仓库入职手册
type: 概念卡
tags:
  - 概念
  - Agent工程
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · Agentic 工程实践
sources:
  - https://agents.md/
  - https://github.com/agentsmd/agents.md
publish: true
---

# AGENTS.md

`AGENTS.md` 是放在仓库里、写给编码 agent 看的入职手册：怎么构建、怎么测试、有哪些约定和红线。给人看的仍然是 `README.md`。

## 定义

它是一层很薄的弱标准：统一的是文件名，不是强制字段，也没有严格的 schema。OpenAI 把这份约定捐了出来，Cursor、GitHub Copilot、Codex 等都会读。它现在位于 Linux Foundation 下的 Agentic AI Foundation 名下。官方说明见 [agents.md](https://agents.md/)。

实践上最有用的几条：

- **写短。** 只写 agent 每次都需要的约定。不要用工具的一键初始化生成一大份空话。需要展开的专项流程，做成 [[Skills]]，用到再加载。
- **大仓库可以嵌套。** 根目录一份往往不够，子项目可以各放一份，通常近的那份优先生效。
- **它不是流程引擎。** 单靠一份手册撑不住超大库，更替不了测试和 hooks。
- **各家加载方式并不完全一样。** 有的工具并不原生读取这份文件，需要自行接入，或再并存一份该工具认识的规则文件。

## 和相近概念的差别

- 和 `README.md`：一个对人，一个对 agent，不必合成一篇。
- 和 [[Skills]]：`AGENTS.md` 是每次都可能用到的短手册；Skills 是按任务加载的专项说明。
- 和 Spec Kit、OpenSpec、BMAD 这类框架：那些在管「先规格后实现」的整条流水线，和这份入职手册不是同一层。见 [[薄技能与重框架]]。

相关入口：[[indexes/Agent工程]]。
