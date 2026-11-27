---
title: claude-mem
type: 项目卡
tags:
  - 开源项目
  - 记忆
  - 编码agent
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/thedotmack/claude-mem
publish: true
repo: https://github.com/thedotmack/claude-mem
license: Apache-2.0
stars: 120062
verdict: 「agent 在这个项目里干过什么」型记忆的代表；装上就能用，但要注意它记的是工作轨迹，不是用户偏好
---

# claude-mem

[claude-mem](https://github.com/thedotmack/claude-mem) 用 hooks 捕获编码 agent 在会话里做的每一步（工具调用、改动、结论），用模型压缩成摘要，下次开会话时再按需注入，让 agent 跨会话接上上下文。许可证 Apache-2.0，星标 120,062，截至 2026-11-26（太平洋时间），是 2026 年下半年增长最快的记忆类仓库之一。

## 判断

记忆有两种读者。用户记忆服务「这个人的下一次对话」；agent 记忆服务「这个角色的下一次任务」。claude-mem 属于后者：记工具调用、失败和做法，不记个人偏好。两层的权限也相反，前者跟人走，后者跟角色和项目走。

用之前要想清楚两件事：压缩摘要会花模型调用；注入的历史越多，每轮上下文越重，记忆本身也要有预算。

## 和相邻项目的差别

- 对照 [[Mem0]]：Mem0 偏用户偏好和事实。
- 对照 [[Beacon]]、[[deja-vu]]：同样从会话里取经验，那两个更强调跨工具。

选型见 [[Agent会话归档工具对照]]。入口：[[indexes/开源项目]]。
