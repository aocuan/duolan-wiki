---
title: obsidian-skills
type: 项目卡
tags:
  - 开源项目
  - Skills
  - 笔记
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/obsidianmd/obsidian-skills
publish: true
repo: https://github.com/obsidianmd/obsidian-skills
license: MIT
stars: 54123
verdict: Obsidian 官方给 agent 的技能包，是 Markdown 知识库给 agent 用的最低成本起点
---

# obsidian-skills

[obsidian-skills](https://github.com/obsidianmd/obsidian-skills) 是 Obsidian 官方发布的一组 agent 技能，教编码 agent 正确读写 Obsidian 的开放格式：Markdown 笔记、双链、Bases 和 JSON Canvas。许可证 MIT，星标 54,123，截至 2026-11-26（太平洋时间）。可以用 `npx skills add obsidianmd/obsidian-skills` 安装到支持 [[Skills]] 的工具里。

## 判断

它不是知识库产品，而是让 agent 按笔记库的规矩干活。对「Markdown 仓库 + AGENTS.md + llms.txt」这种薄方案，它是成本最低的一块补充，也是 [[LLM知识库]] 做法的常用基础。

## 和相邻项目的差别

- 对照 [[claude-obsidian]]：后者让模型主动整理整个库；obsidian-skills 只提供读写规范。
- 对照 [[Basic-Memory]]：Basic Memory 把笔记变成跨会话记忆服务。

落地见 [[个人知识库怎么搭]]。地图见 [[Agent知识库项目地图]]。入口：[[indexes/开源项目]]。
