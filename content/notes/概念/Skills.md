---
title: Skills
type: 概念卡
tags:
  - 概念
  - Skills
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · Agentic 工程实践
sources:
  - https://agentskills.io/home
  - https://github.com/agentskills/agentskills
publish: true
---

# Skills

Skills 是给 agent 用的、按需加载的专项说明。典型形态是一个目录，里面有 `SKILL.md`，需要时还可以附带脚本和参考资料。

## 定义

上下文窗口有限，不能把整本方法论一次塞进 [[AGENTS-md|AGENTS.md]]。Skills 的设计就是：**用到再加载**。修测试有一套，做前端有一套，写设计评审又有一套。

开放标准由 Agent Skills 规范描述，见 [agentskills.io](https://agentskills.io/home) 和规范仓库 [agentskills/agentskills](https://github.com/agentskills/agentskills)（Apache-2.0）。Claude Code、Cursor、Codex 等都可以识别同一类文件。

好的 skill 通常很薄：把「怎么干」写成可执行的步骤和硬约束，能交给 lint 或测试的，就不要让模型每次再猜。

## 和相近概念的差别

- 和长提示词：skill 是可安装、可版本管理、可在多个仓库复用的工件，不是聊天里的一段话。
- 和 [[Harness]]：harness 是工位本身（规则、工具、沙箱、钩子）；Skills 是放在工位上、按任务取用的说明书。
- 和重型规格框架：用 Skills 组合工作流，和装一套替你管全程的方法库，是两条路。取舍见 [[薄技能与重框架]]。
- 和会自我演化的 skill 系统：[[WikiSkill]] 这类论文还在探索「从执行轨迹里积累 wiki，再回写 skill」，比手工维护的 `SKILL.md` 更重，不必一上来就上。

前端设计方向的具体串法见 [[前端设计Skills怎么串]]。相关入口：[[indexes/Skills]]。
