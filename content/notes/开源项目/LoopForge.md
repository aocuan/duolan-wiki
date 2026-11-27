---
title: LoopForge
type: 项目卡
tags:
  - 开源项目
  - 派活
  - 编码agent
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/Tencent/LoopForge
publish: true
repo: https://github.com/Tencent/LoopForge
license: MIT（第三方组件除外）
stars: 6052
verdict: 自托管的编码 agent 交付流程：沙箱、角色、人工审批关卡和可复用流程；适合团队把派活和审批固化下来
---

# LoopForge

[LoopForge](https://github.com/Tencent/LoopForge) 是腾讯开源的自托管工作区，让团队用编码 agent 交付软件。在聊天里向主 bot 提需求，它会开一个 Docker 沙箱、拉取仓库、分派给项目角色，最后开 PR。一种做法被证明有效后，可以存成 LOOP，也就是由 agent、脚本和人工审批关卡组成的可复用交付流程。底层执行交给 CodeBuddy、Codex、Claude Code、OpenCode 等命令行 agent。许可证是 MIT，第三方组件按各自许可证。星标 6,052，截至 2026-11-26（太平洋时间）。

## 判断

单次让 agent「修个 bug」，结果取决于那一次运行：可能跳过计划、忘了测试、自己评自己。LoopForge 把计划、测试、评审和审批写成流程，并让每次改动都能追溯回原始需求，还能统计交付和成本。它和 [[Multica]]、[[Agent-Orchestrator]] 一样属于派活层，特点是审批关卡和流程复用。

品类见 [[AI-Native组织对照]]。入口：[[indexes/开源项目]]。
